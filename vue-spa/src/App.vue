<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/about-nest/project">About-project</router-link> |
      <router-link to="/about-nest/projects/images">About-project-images</router-link>
      <!-- <button @click="go('/')">Home</button> |
      <button @click="go('/about')">About</button> |
      <button @click="go('/about-nest/project')">About-project</button> |
      <button @click="go('/about-nest/projects/images')">About-project-images</button> -->
    </div>
    <router-view/>
  </div>
</template>
<script>
export default {
  name: 'App',
  methods: {
    go (link) {
      this.$router.push({
        path: link
      })
    }
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
