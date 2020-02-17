<template>
  <div id="app">
    <SideBar/>
  </div>
</template>

<script>
import SideBar from './components/SideBar.vue'

export default {
  name: 'App',
  components: {
    SideBar
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
padding: 0;
}
</style>
