<template>
  <div>
    <div class="display">
      <input v-model="operand1" />
      <input v-model="operand2" />
      = {{ result }}
    </div>
    <div class="keyboard">
      <button v-on:click="result = parseInt(operand1) + parseInt(operand2)">
        +
      </button>
      <button v-on:click="result = operand1 - operand2">-</button>
      <button v-on:click="result = operand1 / operand2">/</button>
      <button v-on:click="result = operand1 * operand2">*</button>
      <button v-on:click="result = operand1 ** operand2">^</button>
      <button v-on:click="result = parseInt(operand1 / operand2)">//</button>
    </div>
    <!-- </div> -->
  </div>
</template>

<script>
  export default {
    name: "Calculator",
    data() {
      return {
        operand1: "",
        operand2: "",
        result: 0,
      };
    },
    props: {
      msg: String,
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
