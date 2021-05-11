<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Menu mode="alert-primary" alert="alert" msg="Welcome to Your Vue.js App"/>
    <Menu  mode="alert-danger" msg="Welcome to Your Vue.js App"/>
    <Menu  mode="alert-success" msg="Welcome to Your Vue.js App"/>
    <input class="form-control" v-model="name" type="text" name="">
    <button type="button" @click="clickMe()" class="btn btn-primary"></button>
    <h1>Full Name: {{name}}</h1>
    <li v-for="item in items" :key="item">{{item}}</li>
  </div>
</template>

<script>
import Menu from './components/Menu.vue'
export default {
  name: 'App',
  components: {
    Menu
  },
  data(){
    return{
      name: "Nhat",
     items: [
      'Nhat','Bui'
    ]
    }
  },
  methods:{
    clickMe(){
      console.log(this.name)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
