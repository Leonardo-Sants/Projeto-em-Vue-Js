<template>
  <div id="app">
    <Header></Header>
    <Home></Home>
    <Footer></Footer>
  </div>
</template>

<script>
import './styles/global.css';

import Header from './components/HeaderComponent'
import Home from './pages/home.vue'
import Footer from './components/footerComponent.vue'


export default {
  name: 'App',
  components: {
    Header,
    Home,
    Footer
  }
}
</script>


