<template>
  <nav>
    <router-link to="/">vue3+ts</router-link> |
    <router-link to="/advanced">vue3+ts+decorator</router-link>
  </nav>
  <div class="router-view-wrapper">
    <router-view/>
  </div>
</template>

<style>

nav {
  padding: 50px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.router-view-wrapper {
  margin-top: 50px;
}
</style>
