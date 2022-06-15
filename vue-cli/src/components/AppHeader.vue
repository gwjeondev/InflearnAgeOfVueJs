<template>
  <header>
    <h1>{{ propsdata }}</h1>
    <p>{{ num }}</p>
    <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
  props: ['propsdata', 'num'],
  methods: {
    sendEvent() {
      this.$emit('pass');
    }
  }
};
</script>

<style>
</style>