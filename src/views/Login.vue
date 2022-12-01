<template>
  <v-facebook-login
    app-id="687646526313011"
    @sdk-init="handleSdkInit"
    @login="handleLogin"
  ></v-facebook-login>
</template>

<script>
import VFacebookLogin from "vue-facebook-login-component";

export default {
  components: {
    VFacebookLogin,
  },
  data: () => ({
    FB: {},
    model: {},
    scope: {},
  }),
  methods: {
    handleSdkInit({ FB, scope }) {
      this.FB = FB;
      this.scope = scope;
    },
    handleLogin(model) {
      console.log(model);
    },
  },
};
</script>