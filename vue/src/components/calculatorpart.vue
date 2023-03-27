<template>
  <div>
    <div class="outputs">
      <div id="operation">{{ calcsign }}</div>
      <div id="box">
        <div id="calc">{{ calc1 }}</div>
        <div id="ans">{{ answer || 0 }}</div>
      </div>
    </div>
    <div class="press">
      <div>
        <h1>simple calculator</h1>
        <button @click="numberup('1')">1</button>
        <button @click="numberup('2')">2</button>
        <button @click="numberup('3')">3</button>
        <button @click="add()">+</button>
      </div>
      <div>
        <button @click="numberup('4')">4</button>
        <button @click="numberup('5')">5</button>
        <button @click="numberup('6')">6</button>
        <button @click="minus()">-</button>
      </div>
      <div>
        <button @click="numberup('7')">7</button>
        <button @click="numberup('8')">8</button>
        <button @click="numberup('9')">9</button>
        <button @click="mutiply()">*</button>
      </div>
      <div>
        <button @click="neg()">+/-</button>
        <button @click="numberup('0')">0</button>
        <button @click="numberdot()">.</button>
        <button @click="divide()">/</button>
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
  name: "calculator",
  data() {
    return {
      answer: "",
      calc1: "",
      calcsign: "",
    };
  },
  methods: {
    clear() {
      this.answer = "";
      (this.calcsign = ""), (this.calc1 = "");
    },
    enter() {
      if (this.calcsign.indexOf("+") === 0) {
        this.answer = +this.calc1 + +this.answer;
        this.calc1 = "";
        this.calcsign = "";
      } else if (this.calcsign.indexOf("-") === 0) {
        this.answer = this.calc1 - this.answer;
        this.calc1 = "";
        this.calcsign = "";
      } else if (this.calcsign.indexOf("*") === 0) {
        this.answer = this.calc1 * this.answer;
        this.calc1 = "";
        this.calcsign = "";
      } else if (this.calcsign.indexOf("/") === 0) {
        this.answer = this.calc1 / this.answer;
        this.calc1 = "";
        this.calcsign = "";
      }
    },
    add() {
      this.calc1 = this.answer;
      this.calcsign = "+";
      this.answer = "";
    },
    minus() {
      this.calc1 = this.answer;
      this.calcsign = "-";
      this.answer = "";
    },
    divide() {
      this.calc1 = this.answer;
      this.calcsign = "/";
      this.answer = "";
    },
    mutiply() {
      this.calc1 = this.answer;
      this.calcsign = "*";
      this.answer = "";
    },
    numberdot() {
      if (this.answer.indexOf(".") === -1) {
        this.answer = this.answer + ".";
      }
    },
    neg() {
      this.answer = this.answer * -1;
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
  background-color: rgb(255, 197, 80);
  font-size: 15px;
}
button:hover {
  background-color: #ff8f1e;
}
#calc {
  float: right;
  margin-left: 360px;
  font-size: 20px;
}
#operation {
  float: left;
}
.outputs {
  display: flex;
  background-color: rgb(255, 244, 227);
  height: 70px;
}
</style>
