<template>
  <div id="app">
  <h1>Joke App</h1>
  <button @click="showJoke">Show Joke</button>
  <div v-if="joke"></div>
  <p>{{ joke }}</p>
  </div>
</template>
<script>
import axios from "axios";
import Vue from 'vue'
Vue.prototype.$http = axios;
Vue.prototype.axios = axios;
export default {
  data () {
    return {
      joke: ''
    }
  },
  methods: {
     async showJoke() {
        let config = {
          headers: {
            'Accept': 'application/json'
          }
        }
        const joke = await this.$http.get('https://icanhazdadjoke.com', config);
        this.joke = joke.data.joke;
     }
  },
  components: {}
}
</script>

<style>
* {
 margin: 0;
 padding: 0;
 box-sizing:border-box;
}
</style>
