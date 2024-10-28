<template>
  <!-- 
  <HolaMundo />
  <hr />
  <HomeComponent />
  <MusicaComponent />
  <CineComponent />
  <hr /> 
  <img alt="Vue logo" src="./assets/images/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> 
  <hr /> 
  -->
  <h1 style="color: blue">Título Estático</h1>
  <MenuComponent />
  <hr />
  <router-view />
  <hr />
</template>

<script>
import MenuComponent from './components/MenuComponent.vue';

export default {
  name: "App",
  
  components: {
    // HolaMundo, HomeComponent, ... --> con sus respectivos imports
    MenuComponent
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
