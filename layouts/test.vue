<template>
  <div>
    这里是头部区
    <nuxt/>
    这里是尾部区
  </div>
</template>
<script>
  import Footer from '../components/Footer.vue'
  import Header from '../components/Header.vue'
  export default {
    components: {
      Header,
      Footer
    }
  }
</script>
<style>

</style>
