<template>
  <div
    class="container"
    :class="{ 'light-background': !isDarkMode, 'dark-background': isDarkMode }"
  >
    <div class="request">
      Dont't have an account ?
      <router-link to="/request">Request an account</router-link>
    </div>
    <div class="login">
      <img src="@/assets/DCHQ.svg" alt="logo" />
      <h4>Sign into Code</h4>
      <input type="email" placeholder="Email" />
      <input type="password" placeholder="Password" />
      <button>Sign In</button>
      <router-link to="/recover">Forgot your password ?</router-link>
      <button @click="toggleDarkMode">Toggle</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "SignIn",
  data() {
    return { isDarkMode: true };
  },
  methods: {
    toggleDarkMode() {
      this.isDarkMode = !this.isDarkMode;
    },
  },
};
</script>

<style lang="scss" scoped>
.light-background {
  background-color: $light-gray;
}
.dark-background {
  background-color: $dark-blue;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
.login {
  width: 400px;
}
.request {
  position: absolute;
  top: 40px;
  right: 40px;
  color: rgba(255, 255, 255, 0.3);
  a {
    color: #fff;
  }
}
h4 {
  margin: 0;
  font-size: 24px;
  line-height: 34px;
  color: #fff;
}
input {
  background: rgba(255, 255, 255, 0.2);
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-sizing: border-box;
  border-radius: 4px;

  height: 60px;
  width: 100%;

  font-size: 20px;
  color: #fff;
  padding-left: 20px;
  margin-top: 20px;
  &::placeholder {
    color: rgba(255, 255, 255, 0.3);
  }
}
button {
  background: #56ccf2;
  box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.2);
  border-radius: 4px;
  height: 60px;
  width: 100%;
  margin-top: 20px;
  color: #fff;
  font-size: 20px;
  line-height: 24px;
  border: none;
  margin-bottom: 40px;
}
a {
  font-size: 16px;
  line-height: 25px;
  color: rgba(255, 255, 255, 0.3);
  text-decoration: none;
}
</style>
