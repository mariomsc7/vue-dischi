<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from './components/Header.vue'


export default {
  name: 'App',
  components: {
    Header,
    
  }
}
</script>

<style lang="scss">

@import '~@fontsource/poppins/index.css';
@import '~@fontsource/poppins/400.css';

@import '@/scss/general.scss';

</style>
