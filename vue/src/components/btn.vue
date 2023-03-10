<template>
  <div>
    <button type="button" class="btn" >
      {{ number }}
    </button>
  </div>
</template>

<script>
export default {
  name: "button",
  prop: {
    number: String,
  },
};
</script>
<style scoped>
.btn {
  background-color: rgb(227, 196, 255);
  font-size: 35px;
}
</style>
