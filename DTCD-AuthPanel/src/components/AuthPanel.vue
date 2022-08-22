<template>
  <div class="AuthPanel">
    <div class="SectionBackground">
      <img class="BackgroundImage size_big" src="/img/background_big.png" alt="background">
      <img class="BackgroundImage size_middle" src="/img/background_middle.png" alt="background">
      <img class="BackgroundImage size_small" src="/img/background_small.png" alt="background">
    </div>
    <div class="SectionMainContent">
      <div class="ContentWrapper">
        <div class="LogoWrapper">
          <img src="/img/logo.svg" alt="logo DataCAD">
        </div>
        <span class="Annotation">DataCad is extensible data platform powers unified security, full-stack observability and limitless custom applications</span>

        <form
          v-if="typeVisibleForm === 'autorization'"
          class="Form autorization"
          ref="autorizationForm"
        >
          <h1 class="FormTitle">Авторизация</h1>
          <p class="ErrorMessage">{{errorMessage}}</p>

          <base-input
            class="FieldInput"
            label="Имя пользователя"
            required
            ref="login"
            placeholder="Введите имя пользователя"
          ></base-input>
          <base-input
            class="FieldInput"
            label="Пароль"
            required
            ref="password"
            type="password"
            placeholder="Введите пароль"
          ></base-input>
          <!-- <div class="ForgotPassword">
            <base-checkbox checked>Запомнить меня</base-checkbox>
            <base-button
            theme="theme_alfa"
            type="button"
            @click="() => { toggleForms('password_reset') }"
            >Забыли пароль?</base-button>
          </div> -->
          <base-button
            width="full"
            @click="handleLoginSubmitBtnClick"
            :disabled="disabledForm"
          >Войти</base-button>
          <!-- <div class="FormFooter">
            <span class="TextNote">Еще нет аккаунта?</span>
            <base-button
              theme="theme_alfa"
              type="button"
              @click="() => { toggleForms('registation') }"
            >Зарегистрироваться</base-button>
          </div> -->
        </form>

        <form
          v-if="typeVisibleForm === 'password_reset'"
          class="Form password_reset"
        >
          <h1 class="FormTitle">Сброс пароля</h1>
          <base-input
            class="FieldInput"
            label="Электронная почта или имя пользователя"
            placeholder="Введите имя пользователя"
          ></base-input>
          <base-button
            size="big"
            width="full"
          >Сбросить пароль</base-button>
          <div class="FormFooter">
            <base-button
              theme="theme_alfa"
              size="small"
              type="button"
              @click="() => { toggleForms('autorization') }"
            >
              <svg slot="icon-left" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M8.28809 12L14.2981 18.01L15.7121 16.596L11.1121 11.996L15.7121 7.39599L14.2981 5.98999L8.28809 12Z" fill="#0579F7"/>
              </svg>
              Вернуться на страницу авторизации
            </base-button>
          </div>
        </form>

        <form
          v-if="typeVisibleForm === 'registation'"
          class="Form registation"
        >
          <h1 class="FormTitle">Регистрация</h1>
          <base-input
            class="FieldInput"
            label="Ваше имя*"
            ref="login"
            placeholder="Введите ваше имя"
          ></base-input>
          <base-input
            class="FieldInput"
            label="Имя пользователя*"
            placeholder="Введите имя пользователя"
          ></base-input>
          <base-input
            class="FieldInput"
            label="Название организации"
            placeholder="Введите название организации"
          ></base-input>
          <base-input
            class="FieldInput"
            label="Пароль*"
            ref="password"
            type="password"
            placeholder="Введите пароль"
          ></base-input>
          <base-input
            class="FieldInput"
            label="Повторите пароль*"
            ref="password"
            type="password"
            placeholder="Введите пароль еще раз"
          ></base-input>
          <span class="Note">* – обязательное поле</span>
          <base-button size="big" width="full">Зарегистрироваться</base-button>
          <div class="FormFooter">
            <span class="TextNote">Уже есть аккаунт?</span>
            <base-button
              theme="theme_alfa"
              type="button"
              @click="() => { toggleForms('autorization') }"
            >Войти</base-button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AuthPanel',
  data({ $root }) {
    return {
      plugin: $root.plugin,
      typeVisibleForm: 'autorization',
      errorMessage: '',
      disabledForm: false,
    };
  },
  methods: {
    async login() {
      this.errorMessage = '';
      const login = this.$refs.login.value;
      const password = this.$refs.password.value;
      
      if (!login && !password) return;

      try {
        const response = await Application.getSystem('AuthSystem', '0.1.0').authorize(
          login,
          password
        );
  
        if (response) {
          this.plugin.getSystem('RouteSystem', '0.1.0').navigate('/workspaces');
        } else {
          this.errorMessage = 'Неверное имя пользователя или пароль.';
        }
      } catch (error) {
        this.errorMessage = 'Неверное имя пользователя или пароль.';
      }
    },

    toggleForms(typeTargetForm) {
      this.errorMessage = '';
      
      switch (typeTargetForm) {
        case 'password_reset':
        case 'registation':
          this.typeVisibleForm = typeTargetForm;
          break;

        default:
          this.typeVisibleForm = 'autorization';
          break;
      }
    },

    handleLoginSubmitBtnClick(event) {
      event.preventDefault();
      if (this.disabledForm) return;
      
      this.disabledForm = true;
      setTimeout(() => {
        this.disabledForm = false;
      }, 1000);
      
      if (checkForm(this.$refs.autorizationForm) === 0) {
        this.login();
      }
    },
  },
  mounted() {
    this.$refs.autorizationForm.addEventListener('keyup', (event) => {
      if (this.disabledForm) return;

      if (event.code === 'Enter') {
        this.disabledForm = true;
        setTimeout(() => {
          this.disabledForm = false;
        }, 1000);

        if (checkForm(this.$refs.autorizationForm) === 0) {
          this.login();
        }
      }
    });
  },
};

function checkForm(form) {
  if (!form instanceof HTMLElement) return;

  let countFieldErrors = 0;
  form.querySelectorAll(`
    base-input[required],
    base-textarea[required],
    base-select[required],
    base-colorpicker[required],
    date-time-picker[required],
    base-file-loader[required],
    base-range[required],
    base-checkbox[required],
    base-radio[required],
    base-radio-group[required],
    base-switch[required]
  `).forEach((formElement) => {
    formElement.validate && formElement.validate();
    formElement.invalid && countFieldErrors++;
  });

  return countFieldErrors;
}
</script>

<style lang="scss"scoped>

.AuthPanel {
  $xs: 360px;
  $sm: 576px;
  $md: 768px;
  $lg: 992px;
  $xl: 1200px;
  $xxl: 1400px;

  display: flex;
  font-family: 'Proxima Nova';
  height: 100%;
  width: 100vw;
  position: relative;
  overflow: hidden;
  background-color: var(--background_secondary);

  @media (max-width: $lg) {
    flex-direction: column-reverse;
  }

  &,
  *,
  *::after,
  *::before {
    box-sizing: border-box;
  }

  .SectionBackground,
  .SectionMainContent {
    @media (min-width: $lg) {
      width: 50%;
      min-height: 100%;
    }
  }

  .SectionBackground {
    position: relative;
    display: flex;
    overflow: hidden;

    @media (max-width: $lg) {
      overflow: visible;
    }

    .BackgroundImage {
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      min-width: 100%;
      min-height: 100%;

      &.size_big {
  
        @media (max-width: $lg) {
          display: none;
        }
      }
  
      &.size_middle {
        display: none;
  
        @media (max-width: $lg) {
          display: block;
        }
  
        @media (max-width: $sm) {
          display: none;
        }
      }
  
      &.size_small {
        display: none;
  
        @media (max-width: $sm) {
          display: block;
          transform: translate(-50%, 50%);
        }

        @media (max-width: $sm) {
          transform: translate(-50%, 30%);
        }

        @media (max-width: $xs) {
          transform: translate(-50%, 0%);
        }
      }
    }
  }

  .SectionMainContent {
    display: flex;
    padding: 32px 20px;
    margin: auto;
    z-index: 1;

    @media (max-width: $md) {
      margin-top: 26%;
    }
    @media (max-width: $xs) {
      margin-top: 32px;
    }
  }

  .ContentWrapper {
    max-width: 397px;
    margin: auto;
  }

  .Annotation {
    text-align: center;
    display: inline-block;
    color: var(--text_secondary);
    font-size: 15px;
    line-height: 1.2;
    padding-bottom: 64px;

    @media (max-width: $sm) {
      padding-bottom: 32px;
    }
  }

  .Form {
    text-align: left;
    background-color: var(--background_main);
    padding: 32px;
    box-shadow: 1px 1px 2px rgba(8, 18, 55, 0.12), 0px 4px 12px rgba(8, 18, 55, 0.12);
    border-radius: 16px;

    .FormTitle,
    .ForgotPassword,
    .FieldInput,
    .Note,
    .ErrorMessage:not(:empty) {
      padding-bottom: 16px;
    }

    .FormFooter {
      padding-top: 16px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      column-gap: 5px;
      row-gap: 10px;
    }

    .TextNote {
      color: var(--text_secondary);
      font-size: 13px;
    }

    .FormTitle {
      font-weight: 600;
      font-size: 24px;
      line-height: 1.25;
      margin: 0;
      color: var(--title);
    }

    .ForgotPassword {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      column-gap: 5px;
      row-gap: 10px;
    }

    .Note {
      font-size: 15px;
      color: var(--text_secondary);
      line-height: 1.2;
      display: inline-block;
    }

    .ErrorMessage {
      margin: 0;
      color: var(--danger);
      opacity: 0;
      padding: 0;
      transition: padding .3s,
                  opacity 1s;
      
      &:not(:empty) {
        opacity: 1;
      }
    }
  }

  .LogoWrapper {
    text-align: center;
    padding-bottom: 24px;
  }

  .Logo {
    max-width: 100%;
  }
}
</style>