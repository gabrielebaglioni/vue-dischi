<template>
  <div id="app">
    <BaseHeaderVue></BaseHeaderVue>
    <BaseMain></BaseMain>
  </div>
</template>

<script>
import BaseHeaderVue from './components/blocks/BaseHeader.vue'
import BaseMain from './components/blocks/BaseMain.vue' 


export default {
  
  name: 'App',
  components: {
    BaseHeaderVue,
    BaseMain
}
}
</script>

<style lang="scss">

 @import '../src/assets/style/global.scss' ;

</style>
