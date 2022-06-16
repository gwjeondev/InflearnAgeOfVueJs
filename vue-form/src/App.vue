<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username" />
    </div>
    <div>
      <label for="password">pw: </label>
      <input id="password" type="password" v-model="password" />
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    submitForm() {
      const url = 'https://jsonplaceholder.typicode.com/users';
      //e.preventDefault(); form element에 디렉티브 속성에 .prevent를 추가해주면 동일한 기능을 보장한다.
      console.log(this.username, this.password);
      axios
        .post(url, {
          username: this.username,
          password: this.password
        })
        .then((res) => {
          console.log(res);
        })
        .catch((err) => {
          console.log(err);
        });
    }
  }
};
</script>

<style>
</style>