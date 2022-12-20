<script setup lang="ts">
</script>

<template>
  <header class="header">
    <router-link class="link" to="/">Home</router-link>
    <router-link  class="link" to="/test">Test</router-link>
  </header>
  <router-view />
</template>

<style scoped>
.header {
  background-color: rgb(36, 36, 36);
  height: 5em;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
}

.link {
  margin: 0 1em;
  color: white;
  text-decoration: none;
  transition: all 0.5s;
}

.link:hover {
  color: aquamarine;
}
</style>
