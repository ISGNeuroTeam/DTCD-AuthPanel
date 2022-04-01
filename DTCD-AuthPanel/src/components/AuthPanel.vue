<template>
  <div class="AuthPanel">
    <div class="SectionImage">
      <img class="SectionImage big_screen" src="./images/background_big.png" alt="background">
      <img class="SectionImage small_screen" src="./images/background_small.png" alt="background">
    </div>
    <div class="SectionContent">
      <div class="SectionContainer">
        <svg class="Logo" width="169" height="38" viewBox="0 0 169 38" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" clip-rule="evenodd" d="M18.6295 3.62461C18.6295 1.95584 19.9823 0.603027 21.6511 0.603027L24.6727 25.9363C24.6727 32.5988 19.2614 37.9998 12.5863 37.9998C5.91123 37.9998 0.5 32.5988 0.5 25.9363C0.5 19.2738 5.91123 13.8728 12.5863 13.8728C14.7878 13.8728 16.8518 14.4603 18.6295 15.4867V3.62461ZM21.6511 0.603027L24.6727 25.9295V3.62461C24.6727 1.95584 23.3199 0.603027 21.6511 0.603027ZM12.5864 31.9682C15.9239 31.9682 18.6295 29.2677 18.6295 25.9364C18.6295 22.6052 15.9239 19.9047 12.5864 19.9047C9.24883 19.9047 6.54321 22.6052 6.54321 25.9364C6.54321 29.2677 9.24883 31.9682 12.5864 31.9682Z" fill="#0579F7"/>
          <path fill-rule="evenodd" clip-rule="evenodd" d="M15.608 4.52393C13.9392 4.52393 12.5864 5.87673 12.5864 7.54551V19.9047C12.5865 19.9047 12.5865 19.9047 12.5865 19.9047C15.9139 19.9047 18.6133 22.5889 18.6296 25.9062V7.54551C18.6296 5.87673 17.2768 4.52393 15.608 4.52393Z" fill="#459BF7"/>
          <path fill-rule="evenodd" clip-rule="evenodd" d="M9.5648 8.14282C7.89602 8.14282 6.54321 9.49563 6.54321 11.1644V25.9364C6.54321 22.6052 9.24883 19.9047 12.5864 19.9047V11.1644C12.5864 9.49563 11.2336 8.14282 9.5648 8.14282Z" fill="#78B9FF"/>
          <path fill-rule="evenodd" clip-rule="evenodd" d="M88.3894 38.0001C84.9435 38.0001 82.1405 36.9272 79.9804 34.7813C77.8717 32.5843 76.8173 29.6721 76.8173 26.0445C76.8173 22.4169 77.846 19.5558 79.9032 17.461C82.0119 15.3151 84.7635 14.2422 88.1579 14.2422C90.5752 14.2422 92.6839 15.0852 94.4839 16.7712C94.6897 16.1581 95.0754 15.6472 95.6412 15.2385C96.2069 14.8297 96.8755 14.6253 97.647 14.6253C98.6756 14.6253 99.4985 14.9319 100.116 15.545C100.784 16.107 101.119 16.7968 101.119 17.6143V35.0112C101.119 35.8798 100.784 36.5951 100.116 37.1571C99.4985 37.7191 98.6756 38.0001 97.647 38.0001C95.9497 38.0001 94.8954 37.2593 94.4839 35.7776C92.8382 37.2593 90.8066 38.0001 88.3894 38.0001ZM92.8639 30.183C91.8867 31.2559 90.5752 31.7924 88.9294 31.7924C87.335 31.7924 86.0235 31.2559 84.9949 30.183C84.0177 29.059 83.5291 27.6795 83.5291 26.0445C83.5291 24.3585 84.0177 23.0045 84.9949 21.9827C86.0235 20.9608 87.335 20.4499 88.9294 20.4499C90.5752 20.4499 91.8867 20.9608 92.8639 21.9827C93.8411 23.0045 94.3297 24.3585 94.3297 26.0445C94.3297 27.6795 93.8411 29.059 92.8639 30.183Z" fill="#0579F7"/>
          <path d="M68.3402 38.0001C66.1287 38.0001 64.3029 37.3615 62.8628 36.0842C61.4227 34.8069 60.7027 32.8398 60.7027 30.183V21.906C60.7027 21.3951 60.4455 21.1396 59.9312 21.1396H58.774C57.8483 21.1396 57.1539 20.8586 56.6911 20.2966C56.2282 19.7346 55.9967 19.0193 55.9967 18.1507C55.9967 17.2311 56.2282 16.4902 56.6911 15.9282C57.1539 15.3151 57.8483 15.0085 58.774 15.0085H59.9312C60.4455 15.0085 60.7027 14.7531 60.7027 14.2422V8.5709C60.7027 7.70232 61.0113 6.96148 61.6285 6.34837C62.2456 5.73527 63.0428 5.42871 64.02 5.42871C64.9972 5.42871 65.7944 5.73527 66.4116 6.34837C67.0802 6.91039 67.4145 7.65123 67.4145 8.5709V14.2422C67.4145 14.7531 67.6716 15.0085 68.1859 15.0085H71.0404C71.9147 15.0085 72.6347 15.3151 73.2005 15.9282C73.8176 16.5413 74.1262 17.2822 74.1262 18.1507C74.1262 19.0193 73.8176 19.7346 73.2005 20.2966C72.6347 20.8586 71.889 21.1396 70.9632 21.1396H68.1859C67.6716 21.1396 67.4145 21.3951 67.4145 21.906V29.1101C67.4145 30.0297 67.5688 30.6684 67.8773 31.026C68.2374 31.3837 68.6745 31.5625 69.1888 31.5625C69.3946 31.5625 69.806 31.5114 70.4232 31.4092C71.0404 31.2559 71.4261 31.1793 71.5804 31.1793C72.4033 31.1793 73.0976 31.4859 73.6634 32.099C74.2291 32.7121 74.512 33.4529 74.512 34.3215C74.512 34.9857 74.3062 35.5988 73.8948 36.1608C73.5348 36.7228 72.9433 37.1316 72.1204 37.387C71.4518 37.5914 70.8089 37.7447 70.1917 37.8469C69.5746 37.949 68.9574 38.0001 68.3402 38.0001Z" fill="#0579F7"/>
          <path fill-rule="evenodd" clip-rule="evenodd" d="M40.1726 38.0001C36.7267 38.0001 33.9237 36.9272 31.7636 34.7813C29.6549 32.5843 28.6006 29.6721 28.6006 26.0445C28.6006 22.4169 29.6292 19.5558 31.6865 17.461C33.7951 15.3151 36.5467 14.2422 39.9412 14.2422C42.3584 14.2422 44.4671 15.0852 46.2672 16.7712C46.4729 16.1581 46.8587 15.6472 47.4244 15.2385C47.9901 14.8297 48.6588 14.6253 49.4302 14.6253C50.4588 14.6253 51.2817 14.9319 51.8989 15.545C52.5675 16.107 52.9018 16.7968 52.9018 17.6143V35.0112C52.9018 35.8798 52.5675 36.5951 51.8989 37.1571C51.2817 37.7191 50.4588 38.0001 49.4302 38.0001C47.733 38.0001 46.6787 37.2593 46.2672 35.7776C44.6214 37.2593 42.5899 38.0001 40.1726 38.0001ZM44.6471 30.183C43.6699 31.2559 42.3584 31.7924 40.7126 31.7924C39.1183 31.7924 37.8068 31.2559 36.7781 30.183C35.801 29.059 35.3124 27.6795 35.3124 26.0445C35.3124 24.3585 35.801 23.0045 36.7781 21.9827C37.8068 20.9608 39.1183 20.4499 40.7126 20.4499C42.3584 20.4499 43.6699 20.9608 44.6471 21.9827C45.6243 23.0045 46.1129 24.3585 46.1129 26.0445C46.1129 27.6795 45.6243 29.059 44.6471 30.183Z" fill="#0579F7"/>
          <path d="M133.551 0.925785H139.977L146.791 37.6771H141.142L140.128 31.0928H133.4L132.429 37.6771H126.758L133.551 0.925785ZM139.481 26.897L136.893 8.58589H136.656L134.047 26.897H139.481Z" fill="#17569B"/>
          <path d="M150.601 0.925785H156.402C157.279 0.925785 158.185 0.954474 159.119 1.01185C160.068 1.05489 160.988 1.20551 161.88 1.46371C162.785 1.72192 163.634 2.12357 164.424 2.66867C165.229 3.19943 165.934 3.95253 166.538 4.92798C167.141 5.88908 167.616 7.10838 167.961 8.58589C168.32 10.0491 168.5 11.8422 168.5 13.9652V24.6377C168.5 26.7607 168.32 28.561 167.961 30.0385C167.616 31.516 167.141 32.7353 166.538 33.6964C165.934 34.6575 165.229 35.4106 164.424 35.9557C163.634 36.4865 162.785 36.881 161.88 37.1392C160.988 37.3974 160.068 37.5552 159.119 37.6125C158.185 37.6556 157.279 37.6771 156.402 37.6771H150.601V0.925785ZM157.61 33.7825C158.616 33.7825 159.443 33.6534 160.09 33.3952C160.751 33.137 161.269 32.6851 161.642 32.0396C162.031 31.3797 162.297 30.4904 162.44 29.3715C162.584 28.2382 162.656 26.8109 162.656 25.0896V13.6855C162.656 11.9641 162.584 10.544 162.44 9.42506C162.297 8.29182 162.031 7.40245 161.642 6.75693C161.269 6.09707 160.751 5.63804 160.09 5.37984C159.443 5.12163 158.616 4.99253 157.61 4.99253H156.187V33.7825H157.61Z" fill="#17569B"/>
          <path d="M117.018 37.9998C116.443 37.9998 115.817 37.9496 115.142 37.8492C114.48 37.7632 113.812 37.5695 113.136 37.2683C112.475 36.967 111.835 36.5438 111.217 35.9987C110.613 35.4393 110.074 34.7077 109.599 33.804C109.139 32.9003 108.766 31.7886 108.478 30.4688C108.205 29.1348 108.068 27.5497 108.068 25.7135V12.6957C108.068 10.8452 108.212 9.26727 108.5 7.96189C108.787 6.64218 109.168 5.53763 109.643 4.64825C110.117 3.74453 110.663 3.02729 111.282 2.49654C111.9 1.96578 112.539 1.56413 113.201 1.29158C113.862 1.00468 114.516 0.818199 115.163 0.73213C115.824 0.646062 116.435 0.603027 116.996 0.603027C118.463 0.603027 119.685 0.811027 120.662 1.22702C121.654 1.62868 122.445 2.18812 123.034 2.90536C123.638 3.60826 124.062 4.43308 124.307 5.37984C124.604 6.07602 125.132 8.53106 124.867 12.7817H119.756L119.692 10.9097C119.692 8.88713 119.469 7.37376 119.023 6.36963C118.578 5.36549 117.923 4.86342 117.061 4.86342C116.543 4.86342 116.09 4.96384 115.702 5.16466C115.314 5.36549 114.991 5.70977 114.732 6.19749C114.473 6.67087 114.272 7.30204 114.128 8.091C113.999 8.87996 113.934 9.86258 113.934 11.0388V27.8222C113.934 28.9698 113.984 29.9237 114.085 30.684C114.2 31.4443 114.38 32.0539 114.624 32.513C114.868 32.972 115.185 33.3019 115.573 33.5028C115.975 33.6892 116.457 33.7825 117.018 33.7825C117.377 33.7825 117.722 33.7036 118.053 33.5458C118.384 33.3737 118.671 33.1155 118.915 32.7712C119.174 32.4126 119.375 31.9679 119.519 31.4371C119.677 30.892 119.756 30.2537 119.756 29.5221V25.9287H124.867V29.3284C124.867 32.2835 124.192 34.4639 122.84 35.8696C121.489 37.2754 119.548 37.9855 117.018 37.9998Z" fill="#17569B"/>
        </svg>
        <span class="Annotation">DataCad is extensible data platform powers unified security, <br> full-stack observability and limitless custom applications</span>

        <form 
          v-if="typeVisibleForm === 'autorization'"
          class="PanelWindow autorization"
        >
          <h1 class="WindowTitle">Авторизация</h1>
          <base-input class="WindowInput" ref="login" label="Имя пользователя" placeholder="Введите имя пользователя"></base-input>
          <base-input class="WindowInput" ref="password" label="Пароль" type="password" placeholder="Введите пароль"></base-input>
          <base-checkbox checked>Запомнить меня</base-checkbox>
          <base-button
            class="ButtonForgotPassword"
            theme="theme_alfa"
            type="button"
            @click="() => { toggleForms('password_reset') }"
          >Забыли пароль?</base-button>
          <base-button
            size="big"
            width="full"
            type="button"
            @click="login"
          >Войти</base-button>
          <base-button
            theme="theme_alfa"
            type="button"
            @click="() => { toggleForms('registation') }"
          >Зарегистрироваться</base-button>
        </form>

        <form
          v-if="typeVisibleForm === 'password_reset'"
          class="PanelWindow password_reset"
        >
          <h1 class="WindowTitle">Сброс пароля</h1>
          <base-input
            class="WindowInput"
            label="Электронная почта или имя пользователя"
            placeholder="Введите имя пользователя"
          ></base-input>
          <base-button
            size="big"
            width="full"
          >Сбросить пароль</base-button>
          <base-button
            theme="theme_alfa"
            type="button"
            @click="() => { toggleForms('autorization') }"
          >Войти</base-button>
        </form>

        <form
          v-if="typeVisibleForm === 'registation'"
          class="PanelWindow registation"
        >
          <h1 class="WindowTitle">Регистрация</h1>
          <base-input class="WindowInput" ref="login" label="Ваше имя*" placeholder="Введите ваше имя"></base-input>
          <base-input class="WindowInput" label="Имя пользователя*" placeholder="Введите имя пользователя"></base-input>
          <base-input class="WindowInput" label="Название организации" placeholder="Введите название организации"></base-input>
          <base-input class="WindowInput" ref="password" label="Пароль*" type="password" placeholder="Введите пароль"></base-input>
          <base-input class="WindowInput" ref="password" label="Повторите пароль*" type="password" placeholder="Введите пароль еще раз"></base-input>
          <span class="Note">* – обязательное поле</span>
          <base-button size="big" width="full">Зарегистрироваться</base-button>
          <base-button
            theme="theme_alfa"
            type="button"
            @click="() => { toggleForms('autorization') }"
          >Войти</base-button>
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
    };
  },
  methods: {
    async login() {
      const login = this.$refs.login.value;
      const password = this.$refs.password.value;
      if (!login && !password) {
        console.log('Login or password must be filled in order to login');
        return;
      }
      const response = await Application.getSystem('AuthSystem', '0.1.0').authorize(
        login,
        password
      );

      if (response) {
        this.plugin.getSystem('RouteSystem', '0.1.0').navigate('/workspaces');
      }
    },

    toggleForms(typeTargetForm) {
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
  },
};
</script>

<style lang="scss"scoped>

.AuthPanel {
  display: flex;
  align-items: center;
  font-family: 'Proxima Nova';
  margin: 0 auto;

  @media (max-width: 1000px) {
    flex-direction: column-reverse;
    padding-top: 250px;
  }

  @media (max-width: 600px) {
    padding-top: 64px;
  }

  &,
  *,
  *::after,
  *::before {
    box-sizing: border-box;
  }

  br {
    @media (max-width: 600px) {
      display: none;  
    }
  }

  .SectionImage {
    width: 950px;
    min-width: 500px;
    display: flex;

    @media (max-width: 1000px) {
      width: auto;
    }

    @media (max-width: 600px) {
      margin-top: -32%;  
    }
 
    &.big_screen {
      height: 1080px;
      width: 950px;
      min-width: 500px;

      @media (max-width: 1000px) {
        display: none;
      }
    }

    &.small_screen {
      display: none;

      @media (max-width: 1000px) {
        display: block;
        width: 1000px;
        min-width: 360px;
      }

      @media (max-width: 600px) {
        margin-top: -10%;
        height: 600px;
        width: auto;
      }
    }
  }

  .SectionContent {
    width: 970px;

    @media (max-width: 1000px) {
      width: auto; 
    }

    .SectionContainer {
      width: 397px;
      text-align: center;
      margin: 0 auto;

      @media (max-width: 600px) {
        width: 320px;
      }

      .Annotation {
        display: inline-block;
        color: var(--text_secondary);
        font-size: 15px;
        line-height: 1.2;
        padding: 24px 0 64px;

        @media (max-width: 600px) {
          padding: 24px 0 32px;
        }
      }

      .PanelWindow {
        text-align: left;
        background-color: var(--background_main);
        padding: 32px;
        box-shadow: 1px 1px 2px rgba(8, 18, 55, 0.12), 0px 4px 12px rgba(8, 18, 55, 0.12);
        border-radius: 16px;

        &.autorization{
          margin-bottom: 39px;

          @media (max-width: 600px) {
            margin-bottom: 0;
          }
        }

        &.password_reset {
          @media (max-width: 1000px) {
            margin-bottom: 141px; 
          }
          @media (max-width: 600px) {
            margin-bottom: -3%; 
          }
        }

        &.registation {
          @media (max-width: 1000px) {
            margin-bottom: -51%;
          }
          @media (max-width: 600px) {
            margin-bottom: -9%; 
          }
        }

        .WindowTitle {
          font-weight: 600;
          font-size: 24px;
          line-height: 1.25;
          padding-bottom: 16px;
          margin: 0;
        }

        .WindowInput {
          padding-bottom: 16px;
        }

        .ButtonForgotPassword {
          float: right;
          padding-bottom: 16px;
        }

        .Note {
          font-size: 15px;
          line-height: 18;
          color: var(--text_secondary);
          line-height: 1.2;
          padding-bottom: 16px;
          display: inline-block;
        }
      }
    } 
  }
}
</style>