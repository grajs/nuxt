<template>
  <div id="app"  class="wrapper">
    <headContent></headContent>
    <keep-alive>
      <router-view style="margin-bottom: 56px" v-if="$route.meta.keepAlive">
      </router-view>
    </keep-alive>
    <router-view style="margin-bottom: 56px" v-if="!$route.meta.keepAlive">
    </router-view>
  </div>
</template>

<script>
  import './assets/style/common.css'
  import 'font-awesome/css/font-awesome.min.css'
  import headContent from './components/head'

  export default {
    components: {headContent}
  }
</script>

<style scoped>
</style>