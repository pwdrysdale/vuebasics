<template>
  <div>
    <div v-for="todo in todos" v-bind:todos="todo" v-bind:key="todo.id">
      <h1 class="head">{{ todo.text }}</h1>
      <h3>{{ todo.completed ? "She done!" : "Yet to do..." }}</h3>
    </div>
    <h1 style="background-color: red; color: white">Alternative Render</h1>
    <div v-for="todo in todos" v-bind:todos="todo" v-bind:key="todo.id">
      <ListItem :todo="todo" />
    </div>
  </div>
</template>

<script>
import ListItem from "./ListItem.vue";

export default {
  name: "ToDos",
  data: () => ({
    todos: [
      {
        id: 1,
        text: "Todo one",
        completed: false,
      },
      { id: 2, text: "todo two", completed: true },
      { id: 3, text: "todo three", completed: false },
    ],
  }),
  components: {
    ListItem,
  },
};
</script>

<style scoped>
.head {
  background-color: blue;
  color: white;
}
</style>
