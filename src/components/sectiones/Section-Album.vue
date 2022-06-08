<template>
   <section class="section">
       <div class="container py-5">
          <div class="row gap-4 justify-content-center">
               <CardAlbum class="col-12 col-md4 col-xl-2" v-for="(album, index) in filterAlbum " :key="index " :album="album" />
          </div>
       </div>
   </section>
</template>

<script> 
 import axios from 'axios';
import CardAlbum from '../common/CardAlbum.vue';
import select from '../shared/select';


export default {
    name: "Section-Album.vue",
     components: { CardAlbum },
    data() {
        return {
            albums: [],
            select
        };
    },
    created() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((response) => {
            // handle success
            this.albums = response.data.response;
        })
            .catch((error) => {
            // handle error
            console.log(error);
        });
    },
    computed:{
      filterAlbum(){
        return this.albums.filter((elm) => elm.genre === this.select.value || this.select.value === 'All');
      }
  },
   
}
</script>

<style lang="scss" scoped>
 .section{

 }
 .row{
    display: flex;
 }
</style>