<template>
  <div id="app">
    <header>
      <span>Learn Vue JS</span>
    </header>
    <main>
      <router-view></router-view>
    </main>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
  @import './assets/css/main.css';
</style>
