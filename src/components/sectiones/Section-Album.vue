<template>
   <section class="section">
       <div class="container py-5">
          <div class="row gap-4 justify-content-center">
               <CardAlbum class="col-12 col-md4 col-xl-2" v-for="(album, index) in albums " :key="index " :album="album" />
          </div>
       </div>
   </section>
</template>

<script> 
 import axios from 'axios';
import CardAlbum from '../common/CardAlbum.vue';


export default {
    name: "Section-Album.vue",
    data() {
        return {
            albums: [],
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
    components: { CardAlbum }
}
</script>

<style lang="scss" scoped>
 .section{

 }
 .row{
    display: flex;
 }
</style>