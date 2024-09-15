<template>
  <div>
    <HeaderComponent>
    </HeaderComponent>
    <HomePage></HomePage>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>

import './styles/global.css'
import HeaderComponent from './components/HeaderComponent.vue';
import HomePage from './pages/Home.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    HomePage,
    FooterComponent
  }
}
</script>

<style>

</style>
