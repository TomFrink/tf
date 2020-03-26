<template>
  <v-app id="app">
    <v-toolbar>
      <v-toolbar-items id="nav">
        <v-btn to="/">Home</v-btn>
        <v-btn to="/about">About</v-btn>
        <v-btn to="/projects">Projects</v-btn>
        <v-btn to="/blog">Blog</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <router-view />
  </v-app>
</template>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 10px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
