<template>
  <div class="card">
     <img :src="album.poster" :alt="album.author">
      <h4 class="my-3">{{album.title}}</h4>
      <h5><small>{{album.author}}<br>{{album.year}}</small></h5>
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
   background-color: #2D3A46;
   text-align: center;
   img{
      width: 100%;
      margin-top: 0.625rem;
   }
   h4{
         color: whitesmoke;

      }
      h5{
         color: grey;
      }
}

</style>