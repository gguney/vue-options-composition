<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Composition from './components/Composition.vue'
import Options from './components/Options.vue'
</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div class="flex">
    <Composition message="Composition Api Component" />
    <Options message="Options Api Component" />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.flex{
  display: flex;
}

.flex--column{
  flex-grow: 1;
}
</style>



