<template>
  <div>
    <label class="answerbox">{{ number }}</label> <input type="text" />
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
