<template>
  <div class="hello">
    <button v-on:click="getData">Click</button>
    <p>{{info.stargazers_count}}</p>
  </div>
</template>

<script>
import axios from 'axios';
/* eslint-disable */
export default {
  name: 'hello',
  data() {
    return {
      info: {
        getData: {}
      }
    };
  },
  methods: {
    getData() {
      axios.get("https://api.github.com/repos/vuejs/vue")
      .then(function (response) {
        console.log(response);
      })
     .catch(function (error) {
        console.log(error);
    });
    },
  }  
};
</script>
