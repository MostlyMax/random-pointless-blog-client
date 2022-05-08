<template>
  <div id="nav-bar">
    <div class="logo"><p>Random Blog Logo</p></div>
    <div id="nav">
        <router-link :to="{ path: '/' }">Home</router-link>
        <router-link :to="{ name: 'What' }">What???</router-link>
        <router-link :to="{ name: 'Post' }">Post</router-link>
    </div>
  </div>
  <router-view/>
</template>

<script>
import Home from './views/Home.vue'
import What from './views/What.vue'
import Post from './views/Post.vue'

export default {
  components: { Home, What, Post },
}
</script>


<style>
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-weight: bold;
  color: #32325c;
  margin: 0;
}

#nav-bar {
  padding: 0;
  display: flex;
  align-items: center;
  background: #acb3d8;
  margin: 0;
}

.logo {
  margin: 10px;
  padding: 5px;
  text-align: center;
  border-radius: 8px;
  align-items: center;
  background:#32325c;
  color: white;
}

#nav {
  margin-left: auto;
  margin-right: 15%;
  padding: 20px;
}

#nav a {
  font-weight: bold;
  color: #32325c;
  padding: 10px;
  border-radius: 4px;
  margin: 5px;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: white;
  background: #ae5fc1;
}
</style>
