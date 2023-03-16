<script setup>
import answer from "./components/answerdis .vue";
import btn from "./components/btncli.vue";

const box = { box: document.getElementById("box") };
const clear = function () {
  document.getElementById("box").innerHTML = "";
};
const click1 = function () {
  document.getElementById("box").innerText("beforeend", `1`);
};
const click2 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `2`);
};
const click3 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `3`);
};
const click4 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `4`);
};
const click5 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `5`);
};
const click6 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `6`);
};
const click7 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `7`);
};
const click8 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `8`);
};
const click9 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `9`);
};
const click0 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `0`);
};
const click00 = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `00`);
};
const clickpoint = function () {
  document.getElementById("box").insertAdjacentHTML("beforeend", `.`);
};
const clickadd = function (a, b) {
  document.getElementById("box").insertAdjacentHTML("beforeend", `+`);
};
const clickminus = function (a, b) {
  document.getElementById("box").insertAdjacentHTML("beforeend", `-`);
};
const clicktimes = function (a, b) {
  document.getElementById("box").insertAdjacentHTML("beforeend", `x`);
};
const clickdiv = function (a, b) {
  document.getElementById("box").insertAdjacentHTML("beforeend", `÷`);
};

const enter = function () {
  document
    .getElementById("box")
    .value.eval(document.getElementById("box").value);
};
</script>

<template>
  <div>
    <div id="box"></div>
    <div class="press">
      <div>
        <h1>simple calculator</h1>
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
        <btn @click="click00()" symbols="00"></btn>
        <btn @click="click0()" symbols="0"></btn>
        <btn @click="clickpoint()" symbols="."></btn>
        <btn @click="clickdiv()" symbols="÷"></btn>
      </div>
      <div>
        <btn @click="clear()" symbols="clear"></btn>
        <btn @click="enter()" symbols="enter"></btn>
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
  height: 325px;
}
</style>
