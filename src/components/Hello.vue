<template>
  <div class="hello">
    <h1>Type 2 numbers and choose operation.</h1>
    <form>
      <input type="text" v-model.number="a">
      <select v-model="operator" @change="calculate">
        <option>+</option>
        <option>-</option>
        <option>*</option>
        <option>/</option>
      </select>
      <input type="text" v-model.number="b">
      <button type="submit" @click.prevent="calculate">Calculate</button>
    </form>
    <h2>Result: {{ a }} {{ operator }} {{ b }} = {{ c }}</h2>
    <pre>
      {{ $data }}
    </pre>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      a: 1,
      b: 2,
      c: null,
      operator: '+',
    };
  },
  methods: {
    calculate() {
      switch (this.operator) {
        case '+':
          this.c = this.a + this.b;
          break;
        case '-':
          this.c = this.a - this.b;
          break;
        case '*':
          this.c = this.a * this.b;
          break;
        case '/':
          this.c = this.a / this.b;
          break;
        default:
          break;
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
