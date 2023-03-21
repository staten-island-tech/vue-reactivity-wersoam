<script setup>
import answer from "./components/calculator.vue";
</script>
<script>
export default {
  name: "app",
  components: {
    calculator,
  },
};
</script>

<template>
  <HelloWorld />
</template>

<style scoped>
#box {
  font-size: 30px;
}
.press {
  background-color: wheat;
  height: 325px;
}
</style>
