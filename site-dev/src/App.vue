<template>
  <div id="app">
    <Header></Header>
    <router-view path="$router.key"></router-view>
    <Footer></Footer>
  </div>
</template>

<script>
import './styles/global.css';

import Header from './components/HeaderComponent'
import Footer from './components/footerComponent.vue'


export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>


