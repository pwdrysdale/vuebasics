<template>
  <div>
    <h1>{{ item.text }}</h1>
    <h3>{{ item.quantity }}</h3>
    <input
      type="checkbox"
      name=""
      id=""
      v-bind:checked="item.completed"
      v-on:change="toggleCompleted"
    />
    <button v-on:click="deleteChild">Delete Item</button>
  </div>
</template>

<script>
export default {
  name: "ListItem",
  props: {
    item: {
      text: String,
      completed: Boolean,
      id: Number,
      quantity: Number,
    },
  },
  methods: {
    deleteChild() {
      this.$emit("deleteitem", this.item.id);
      console.log("Fired in child");
    },
    toggleCompleted() {
      this.$emit("toggleCompleted", this.item.id);
    },
  },
};
</script>
