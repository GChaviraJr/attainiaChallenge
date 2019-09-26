<template>
  <div id="app">
    <h1 msg="Welcome my page!"/>
    <p>
    <router-link to="/">Go to Home Page</router-link>
    <router-link to="/table1"> Go to Table 1 Page</router-link>
    <router-link to="/table2"> Go to Table 2 Page</router-link>
    </p>
    <router-view></router-view>
  </div>
</template>

<script> 
export default {
  computed: {
    username() {
      return this.$route.params.username
    }
  },
  methods: {
    goBack() {
      window.history.length > 1
        ? this.$router.go(-1)
        : this.$router.push('/')
    }
  },
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  
}
</style>
