<template>
  <div>
    <h1>{{ todo.text }}</h1>
    <h3>{{ todo.completed ? "✅" : "❌" }}</h3>
  </div>
</template>

<script>
export default {
  name: "ListItem",
  props: {
    todo: {
      text: String,
      completed: Boolean,
      id: Number,
    },
  },
};
</script>
