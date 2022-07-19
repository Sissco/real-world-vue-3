<template>
  <nav>
    <router-link :to="{ name: 'EventList' }">Events</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link>
  </nav>
  <router-view />
</template>

<style>
/* font */
html {
  font-size: 62.5%;
}

nav,
p,
span {
  font-size: 1.5rem;
}

h1 {
  font-size: 4rem;
}

h4 {
  font-size: 2rem;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
