<template>
<h1>Simple calculator</h1>
<p>
<label for="number1">a :</label><input name="number1" v-model.number="number1" type="number">
</p>
<p>
<label for="number2">b :</label><input name="number2" v-model.number="number2" type="number">
</p>
<button v-on:click="add">+</button>
<button v-on:click="subtract">-</button>
<button v-on:click="multiply">*</button>
<button v-on:click="divide">/</button>
<button v-on:click="potenz">^</button>
<p>
<label for="result">=</label><input name="result" v-model.number="result" readonly type="number">
</p>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      number1: 0,
      number2: 0,
      result: 0
    }
  },
  methods: {
    add () {
      this.result = this.number1 + this.number2
    },
    subtract () {
      this.result = this.number1 - this.number2
    },
    multiply () {
      this.result = this.number1 * this.number2
    },
    divide () {
      this.result = this.number1 / this.number2
    },
    potenz () {
      this.result = this.number1 ** this.number2
    }
  }
}
</script>

<style>
#app {
  font-family:monospace;
  text-align:center;
  background-color: slategrey;
  color:rgba(1, 2, 2, 0.623);
}

label {
  margin: 3px;
  width: 80px;
  display: inline-block;
  text-align: end;
}

input {
  margin: 3px;
  width: 200px;
  border-color:rgba(131, 150, 168, 0.774);
  background-color: transparent;
}
button {
  margin: 4px;
  border-color:rgba(131, 150, 168, 0.774);
  background-color: transparent;
  padding: 12px 20px;
  color:rgb(0, 0, 0);
}
</style>
