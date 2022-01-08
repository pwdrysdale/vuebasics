<template>
  <h1>This is Vue Baby - {{ yeah }}</h1>
</template>

<script>
export default {
  name: "NewDay",
  props: {
    yeah: String,
  },
};
</script>
