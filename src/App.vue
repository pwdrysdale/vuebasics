<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <ImPete name="Pete" />
  <NewDay yeah="Yeah bby" />
  <RenderList />
  <Counter />
  <ComputedAndConditional />
  <ShoppingList />
  <GetDataFromAPI />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import ImPete from "./components/ImPete.vue";
import NewDay from "./components/NewDay.vue";
import RenderList from "./components/RenderList.vue";
import Counter from "./components/Counter.vue";
import ComputedAndConditional from "./components/ComputedAndConditional.vue";
import ShoppingList from "./components/ShoppingList.vue";
import GetDataFromAPI from "./components/GetDataFromAPI.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    ImPete,
    NewDay,
    RenderList,
    Counter,
    ComputedAndConditional,
    ShoppingList,
    GetDataFromAPI,
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
