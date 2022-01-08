<template>
  <h1>Counter</h1>
  <h3>Count: {{ count }}</h3>
  <h3>Interval: {{ interval }}</h3>
  <input
    v-bind:value="interval"
    v-on:input="interval = parseFloat($event.target.value)"
    type="number"
  />
  <button v-on:click="count += interval">Increment</button>
  <button v-on:click="count -= interval">Decrement</button>
</template>

<script>
export default {
  name: "Counter",
  data: () => {
    return {
      count: 0,
      interval: 1,
    };
  },
};
</script>
