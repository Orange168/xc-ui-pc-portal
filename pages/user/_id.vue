<template>
  <div>
    修改了用户{{id}}
  </div>
</template>
<script>
  export default {
    layout: 'test',

    data(){
      return {
        id:''
      }
    },
    mounted(){
      this.id = this.$route.params.id;
      console.log(this.id)
    }
  }
</script>
<style>

</style>
