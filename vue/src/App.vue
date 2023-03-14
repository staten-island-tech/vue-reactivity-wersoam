<script setup>
import btn from "./components/btn.vue";

const click1 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `<h1>1</h1>`);
};
const clear = function () {
  document.getElementById("box").innerHTML = "";
};
const click2 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `<h1>2</h1>`);
};
const click3 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `<h1>3</h1>`);
};
const clickadd = function (a, b) {
  document.getElementById("box").insertAdjacentHTML("beforeend", `<h1>+</h1>`);
};
const enter = function () {
  if ((document.getElementById("box").innerHTML.includes = "+")) {
    let ans = a + b;
    return ans;
  }
  console.log(ans);
};
</script>
<template>
  <div>
    <div id="box"></div>
    <h1>numbers</h1>
    <button @click="click1()">1</button>
    <button @click="click2()">2</button>
    <button @click="click3()">3</button>
    <button @click="clickadd()">+</button>
    <btn @click="clear()" symbols="clear"></btn>
    <btn @click="enter()" symbols="enter"></btn>
  </div>
</template>

<style scoped>
button {
  border-radius: 12px;
}
</style>
