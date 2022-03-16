<template>
  <div>
    <base-input ref="login" label="Login"> </base-input>
    <base-input ref="password" label="Password" type="password"> </base-input>
    <button @click="login">Login</button>
  </div>
</template>

<script>
export default {
  name: 'AuthPanel',
  data({ $root }) {
    return {
      plugin: $root.plugin,
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
  },
};
</script>

<style scoped></style>
