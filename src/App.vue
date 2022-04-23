<script setup>

</script>

<script>
export default {
  data() {
    return {
      darkTheme: false
    }
  },
  methods: {
    toggleTheme() {
      this.darkTheme = !this.darkTheme;
    }
  },
  watch: {
    darkTheme: (isDarkTheme) => {
      document.body.classList = isDarkTheme ? 'dark' : '' ;
    }
  },
  mounted() {
    document.body.classList = this.darkTheme ? 'dark' : '' ;
  }
}
</script>

<template>
  <button @click="toggleTheme">Toggle theme</button>
</template>

<style>
@import 'https://necolas.github.io/normalize.css/8.0.1/normalize.css';
@import './assets/base.css';

#app {
  background-color: var(--main-color);
}

</style>