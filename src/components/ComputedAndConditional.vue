<template>
  <h1>Computed and Conditional Values</h1>
  <button v-on:click="toggleShow">Toggle Show</button>
  <div v-if="show">
    <button v-on:click="getCount">Increment</button>
    <h3>{{ count }}</h3>
  </div>
</template>

<script>
export default {
  name: "ComputedAndConditional",
  data: () => ({
    count: 0,
    show: true,
  }),

  methods: {
    // increase count by one
    getCount: function () {
      return (this.count += 1);
    },

    // toggle show
    toggleShow() {
      this.show = !this.show;
    },
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
button {
  background-color: blue;
  color: white;
  border: none;
  padding: 10px;
  border-radius: 4px;
  margin: 10px;
}
</style>
