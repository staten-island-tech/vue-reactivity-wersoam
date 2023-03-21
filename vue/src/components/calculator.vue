<template>
  <div>
    <div id="box">{{ number || 0 }}</div>
    <div class="press">
      <div>
        <h1>simple calculator</h1>
        <button @click="click1()" symbols="1"></button>
        <button @click="click2()" symbols="2"></button>
        <button @click="click3()" symbols="3"></button>
        <button @click="clickadd()" symbols="+"></button>
      </div>
      <div>
        <button @click="click4()" symbols="4"></button>
        <button @click="click5()" symbols="5"></button>
        <button @click="click6()" symbols="6"></button>
        <button @click="clickminus()" symbols="-"></button>
      </div>
      <div>
        <button @click="click7()" symbols="7"></button>
        <button @click="click8()" symbols="8"></button>
        <button @click="click9()" symbols="9"></button>
        <button @click="clicktimes()" symbols="*"></button>
      </div>
      <div>
        <button @click="click00()" symbols="00"></button>
        <button @click="click0()" symbols="0"></button>
        <button @click="clickpoint()" symbols="."></button>
        <button @click="clickdiv()" symbols="/"></button>
      </div>
      <div>
        <button @click="clear()" symbols="clear"></button>
        <button @click="enter()" value="enter"></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "answer",
  prop: {
    number: String,
  },
  methods: {
    clear() {
      this.number = "";
    },
    add() {
      this.number;
    },
    minus() {
      this.number;
    },
    divide() {
      this.number;
    },
    mutiply() {
      this.number;
    },
    one() {
      this.number;
    },
  },
};
</script>
