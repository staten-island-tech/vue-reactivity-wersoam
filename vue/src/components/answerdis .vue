<template>
  <div>
    <div id="box">{{ number || 0 }}</div>
  </div>
</template>
<script>
export default {
  name: "answer",
  prop: {
    number: String,
  },
};
</script>
