<template>
  <v-app>
    <v-toolbar dark color="teal">
      <span>
        <v-toolbar-side-icon @click="sidebar = !sidebar"></v-toolbar-side-icon>
      </span>
      <span class="hidden-xs-and-down">
        <v-btn class="white--text" color="purple" large depressed outline>{{ app }}</v-btn>
      </span>
    </v-toolbar>
    <v-container fluid>
      <router-view></router-view>
    </v-container>
    <v-footer app>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      app: this.$store.state.app
    }
  }
}
</script>

<style scoped>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
