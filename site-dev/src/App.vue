<template>
  <div id="app">
    <Header></Header>
    <Home></Home>
  </div>
</template>

<script>
import './styles/global.css';

import Header from './components/HeaderComponent'
import Home from './pages/home.vue'


export default {
  name: 'App',
  components: {
    Header,
    Home
  }
}
</script>


