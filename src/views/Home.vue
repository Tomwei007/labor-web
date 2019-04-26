<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div class="home-header" @click="apply()">
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
  },
  data () {
    return {
      name: '',
      person: {
        name: ''
      }
    }
  },
  method: {
    apply () {
      var hello = ''
      console.log(hello)
      if (hello === '') {
        console.log('hello')
      }
    }
  }
}
</script>
<style lang="less" scoped>
.home {
  &-header {
    width: 20px;
    height: 30px;
    background-color: #000;
  }
}
</style>
