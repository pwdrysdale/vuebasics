<template>
  <div>
    <h1>Shopping List</h1>
    <div v-for="item in shoppingList" v-bind="item" v-bind:key="item.id">
      <ShoppingListItem
        :item="item"
        @deleteitem="deleteItem"
        @toggleCompleted="toggleCompleted"
      />
    </div>
  </div>
</template>

<script>
import ShoppingListItem from "./ShoppingListItem.vue";

export default {
  name: "ShoppingList",
  data() {
    return {
      shoppingList: [
        { id: 1, text: "Potatoes", quantity: 2, completed: true },
        { id: 2, text: "Milk", quantity: 1, completed: false },
        { id: 3, text: "Eggs", quantity: 12, completed: false },
        { id: 4, text: "Bread", quantity: 2, completed: true },
        { id: 5, text: "Cheese", quantity: 1, completed: false },
      ],
    };
  },
  methods: {
    deleteItem(id) {
      this.shoppingList = this.shoppingList.filter((item) => item.id !== id);
    },
    toggleCompleted(id) {
      this.shoppingList = this.shoppingList.map((item) =>
        item.id === id ? { ...item, completed: !item.completed } : item
      );
    },
  },

  components: {
    ShoppingListItem,
  },
};
</script>
