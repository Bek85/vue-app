<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <LogoMain />
  <TriggerAlert />
  <AddToCart />
  <LifecycleHooks />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import LogoMain from "@/components/LogoMain";
import TriggerAlert from '@/components/TriggerAlert'
import AddToCart from '@/components/AddToCart';
import LifecycleHooks from "@/components/LifecycleHooks";


export default {
  name: 'App',
  components: {
    HelloWorld, LogoMain, TriggerAlert, AddToCart, LifecycleHooks
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
  margin-top: 60px;
}
</style>
