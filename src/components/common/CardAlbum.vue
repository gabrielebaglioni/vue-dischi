<template>
  <div class="card">
     <img src="https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png" alt="">
     <h3>nome </h3>
     <div>nome album</div>
     <div>anno</div>
  </div>
</template>

<script>
export default {
   name: 'CardAlbum.vue',
   props: {
      album: Object,
   }

}
</script>

<style lang="scss" scoped>
.card{
   img{
      width: 100%;
   }
}

</style>