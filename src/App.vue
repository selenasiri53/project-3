<template>
  <header>
    <h1>Reactivity in Action</h1>
  </header>
  <section id="app">
    <button @click="add(5)">Add 5</button>
    <button @click="add(1)">Add 1</button>
    <!-- 1) Connect the buttons and calculate a value (a number) -->
    <!-- Show "Not there yet" until you reach a result of exactly 37 -->
    <!-- Show "Too much!" if the result is greater than 37 -->
    <p>Result: {{ number }}</p>
    <!-- 2) Watch for changes in "result" and reset the value to 0 after 5 seconds -->
  </section>
</template>

<script>
export default {
  name: 'App',
  components: {},
  data() {
    return {
      number: 0,
    };
  },
  // computed: {
  //     if (this.number < 37) {
  //       return 'Not there yet!';
  //     } else if (this.number > 37) {
  //       return 'Too much!';
  //     } else {
  //       return this.number;
  //     }
  // },
  // watch: {
  //   result(value, oldValue) {
  //     setTimeout(() => {
  //       this.number = 0;
  //     }, 5000);
  //   },
  // },
  methods: {
    add(num) {
      this.number = this.number + num;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
