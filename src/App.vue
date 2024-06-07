<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <div class="main-list">
    <div 
      v-for="item in modelInfo"
      :key="item.name"
      class="model-item"
    >
      <Main :data="{ name: item.name, description: item.description, link: item.link }"/>
    </div>
  </div>
</template>

<script setup lang="ts">
import Main from './components/MainComponent.vue';
import {modelInfo} from './data'


</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body{
  box-sizing: border-box;
  background-image: url('assets/background_Chemistry.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;
}

.main-list {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
</style>
