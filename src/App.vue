<template>
  <div id="app">
    <section>
      <p>Times clicked: {{ count }}</p>
      <button @click="increment">increment</button>
    </section>
    <section>
      <br />
      <button @click="tenTimes">Increment by 10</button>
    </section>
    <section>
      <br />
      <button @click="decrement">Decrement</button>
    </section>
    <section>
      <br />
      <button @click="resetCount">Reset</button>
    </section>
    <section>
      <br />
      <label for="item">Start Typing</label>
      <input type="text" v-model="item" id="item" />
      <div>You typed: {{ item }}</div>
    </section>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      count: 0,
      item: "",
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    resetCount() {
      this.count = 0;
    },
    decrement() {
      this.count--;
    },
    tenTimes() {
      this.count += 10;
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
