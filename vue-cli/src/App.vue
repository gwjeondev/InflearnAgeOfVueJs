<template>
  <!-- template root는 무조건 하나만 있어야함. -->
  <div>
    <!-- {{ str }} -->
    <app-header
      v-bind:propsdata="str"
      v-bind:num="num"
      v-on:pass="addNum"
    ></app-header>
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
      str: 'this is props data',
      num: 0
    };
  },
  methods: {
    addNum() {
      this.num++;
    }
  }
};
</script>

<style>
</style>