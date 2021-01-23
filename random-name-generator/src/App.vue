<template>
  <div id="app">
    <header>
      <div class="container">
        <div class="title">Random Name Generator</div>
        <div class="subtitle">with vuejs</div>
      </div>
    </header>
    <main>
      <div class="container">
        <name-generator></name-generator>
      </div>
    </main>
  </div>
</template>

<script>
import NameGenerator from './components/NameGenerator.vue'

export default {
  name: 'App',
  components: {
    NameGenerator
  }
}
</script>

<style>
*, *::before, *::after {
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px 0;
}

.container {
  width: 100%;
  max-width: 1110px;
  padding: 0 15px;
  margin: 0 auto;
}

.title {
  font-size: 2rem;
}

.subtitle {
  font-size: 1.5rem;
}
</style>
