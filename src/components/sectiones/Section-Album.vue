<template>
   <section>
       <div class="container">
          <div class="row">
             <div class="col">1</div>
             <div class="col">2</div>
             <div class="col">3</div>
             <div class="col">4</div>
             <div class="col">5</div>
          </div>
       </div>
   </section>
</template>

<script> 
 import axios from 'axios';


export default {
   name: 'Section-Album.vue',
    data() {
    return{
        albums: [],
    };
   
 },
   created(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
         // handle success
         this.albums =  response.data ;
      })
      .catch((error) => {
         // handle error
         console.log(error);
      })
      ;
   }
}
</script>

<style lang="scss" scoped>

</style>