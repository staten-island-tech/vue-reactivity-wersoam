<template>
  <button type="button" class="btn">
    {{ symbols }}
  </button>
</template>

<script>
export default {
  name: "button",
  props: {
    symbols: String,
  },
};
</script>

<style scoped>
.btn {
  background-color: rgb(227, 196, 255);
  font-size: 35px;
}
</style>
