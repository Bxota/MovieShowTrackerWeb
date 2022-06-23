<template>
  <title>MST</title>
  <myHeader/>
  <myPage/>
</template>

<script>
import myHeader from './components/myHeader.vue'
import myPage from './components/myPage.vue'

export default {
  name: 'App',
  components: {
    myHeader,
    myPage
  }
}
</script>

<style lang="stylus">
  @import '~assets/index.styl'
</style>
