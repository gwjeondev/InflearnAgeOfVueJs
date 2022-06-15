<template>
  <!-- template root는 무조건 하나만 있어야함. -->
  <div>
    <!-- {{ str }} -->
    <app-header v-bind:propsdata="str"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  components: {
    AppHeader
  },
  data() {
    return {
      str: 'this is props data'
    };
  }
};
</script>

<style>
</style>