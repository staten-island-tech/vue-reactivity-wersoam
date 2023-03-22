<template>
  <div>
    <div id="box">{{ answer || 0 }}</div>
    <div class="press">
      <div>
        <h1>simple calculator</h1>
        <button @click="numberup('1')">1</button>
        <button @click="numberup('2')">2</button>
        <button @click="numberup('3')">3</button>
        <button @click="clickadd()">+</button>
      </div>
      <div>
        <button @click="numberup('4')">4</button>
        <button @click="numberup('5')">5</button>
        <button @click="numberup('6')">6</button>
        <button @click="clickminus()">-</button>
      </div>
      <div>
        <button @click="numberup('7')">7</button>
        <button @click="numberup('8')">8</button>
        <button @click="numberup('9')">9</button>
        <button @click="clicktimes()">*</button>
      </div>
      <div>
        <button @click="numberup('00')">00</button>
        <button @click="numberup('0')">0</button>
        <button @click="numberdot()">.</button>
        <button @click="clickdiv()">/</button>
      </div>
      <div>
        <button @click="clear()">clear</button>
        <button @click="enter()">enter</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "answer",
  data() {
    return { answer: "" };
  },
  methods: {
    clear() {
      this.answer = "";
    },
    add() {
      this.answer;
    },
    minus() {
      this.answer;
    },
    divide() {
      this.answer;
    },
    mutiply() {
      this.answer;
    },
    numberdot() {
      if (this.number.indexOf(".") === -1) {
        this.answer = this.answer + ".";
      } else {
      }
    },

    numberup(number) {
      this.answer = this.answer + number;
    },
  },
};
</script>

<style scoped>
#box {
  font-size: 30px;
}
.press {
  background-color: wheat;
  height: 325px;
}
button {
  background-color: rgb(227, 196, 255);
  font-size: 15px;
}
button:hover {
  background-color: #8b91ff;
}
</style>
