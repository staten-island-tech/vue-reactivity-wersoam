<template>
 <div>{{number || 0 }}</div>
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
    add(){
        this.number
    },
   minus(){
        this.number
    },
    divide(){
        this.number
    },
    mutiply(){
        this.number
    },
    one(){
        this.number
    }
  },
};
</script>
