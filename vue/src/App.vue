<script setup>
import answer from "./components/answer.vue";
import btn from "./components/btn.vue";

const click1 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `1`);
};
const clear = function () {
  document.getElementById("box").innerHTML = "";
};
const click2 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `2`);
};
const click3 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `3`);
};
const clickadd = function (a, b) {
  document.getElementById("box").insertAdjacentHTML("beforeend", `+`);
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
    <div><answer number="" id="box"></answer></div>
    <div class="press">
      <div>
        <h1>numbers</h1>
        <btn @click="click1()" symbols="1"></btn>
        <btn @click="click2()" symbols="2"></btn>
        <btn @click="click3()" symbols="3"></btn>
        <btn @click="clickadd()" symbols="+"></btn>
      </div>
      <div>
        <btn @click="click4()" symbols="4"></btn>
        <btn @click="click5()" symbols="5"></btn>
        <btn @click="click6()" symbols="6"></btn>
        <btn @click="clickminus()" symbols="-"></btn>
      </div>
      <div>
        <btn @click="click7()" symbols="7"></btn>
        <btn @click="click8()" symbols="8"></btn>
        <btn @click="click9()" symbols="9"></btn>
        <btn @click="clicktimes()" symbols="x"></btn>
      </div>
      <div>
        <btn @click="clear()" symbols="clear"></btn>
        <btn @click="enter()" symbols="enter"></btn>
        <btn @click="clickdiv()" symbols="÷"></btn>
      </div>
    </div>
  </div>
</template>

<style scoped>
#box {
  font-size: 30px;
}
.press {
  background-color: wheat;
}
</style>
