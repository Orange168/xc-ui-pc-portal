<template>
  <div>
    用户管理导航
    <nuxt-link :to="'/user/101'">修改</nuxt-link>
    <nuxt-child/>
    <div>name: {{name}}</div>
  </div>
</template>
<script>
  export default {
    layout: 'test',
    // asyncData() {
    //   console.log("==> async方法")
      // var a = await new Promise(function (resolve, reject) {
      //   setTimeout(function () {
      //     resolve(1)
      //   }, 2000)
      // });
    // },
    async asyncData() {
      console.log("async方法")
      var a = await new Promise(function (resolve, reject) {
        setTimeout(function () {
          console.log("1")
          resolve(1)
        },2000)
      });
      var a = await new Promise(function (resolve, reject) {
        setTimeout(function () {
          console.log("2")
          resolve(2)
        },1000)
      });
      return {
        name:'黑马程序员'
      }
    },
    methods: {
      a() {
        return new Promise(function (resolve, reject) {
          setTimeout(function () {
            resolve(1)
          }, 2000)
        })
      },
      b() {
        return new Promise(function (resolve, reject) {
          setTimeout(function () {
            resolve(2)
          }, 1000)
        })
      },

    },
    mounted() {
      // this.a().then(res => {
      //   alert(res)
      //   console.log(res)
      // })
      // this.b().then(res => {
      //   alert(res)
      //   console.log(res)
      // })
    }
  }
</script>
<style>
</style>
