<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
body {
  background-color: $dark-blue;
}
h1 {
  @include heading-1;
}
p {
  @include large-text-bold($purple);
}

#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: $white;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: $white;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
