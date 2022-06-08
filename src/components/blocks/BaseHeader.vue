<template>
  <header class="header">
     <div class="header__container">
        <div class="logo">
           <img src="../../assets/img/spotify-logo.png" alt="Logo">
        </div>
        <div class="row">
           <div class="col-12">
              <SelectImput/>
           </div>
        </div>
       
     </div>
  </header>
  
</template>

<script>
import SelectImput from '../common/SelectImput.vue';
export default {
    name: "BaseHeader",
    components: { SelectImput },
}
</script>

<style lang="scss" scoped>

</style>