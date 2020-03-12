<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
    <v-icon>mdi-menu</v-icon>
    <v-spacer></v-spacer>
    <v-toolbar-title class="white--text">
      <router-link class="title" to="/">Vue Joke App</router-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-icon>mdi-refresh</v-icon>
    </v-app-bar>
    <v-content>
     <Index />
    </v-content>
    <Footer />
  </v-app>
</template>
<script>
import Index from './pages/Index';
import Footer from './components/Footer';
export default {
  name: 'App',

  components: {
    Index,
    Footer
  },
  data: () => ({
    //
  }),
};
</script>
<style scoped>
.title {
  font-size: 50px;
}
</style>
