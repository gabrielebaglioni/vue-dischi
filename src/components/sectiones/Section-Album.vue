<template>
   <section>
       
   </section>
</template>

<script> 
 import axios from 'axios';

export default {
   name: 'Section-Album.vue',
   created(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(function (response) {
         // handle success
         console.log(response.data);
      })
      .catch(function (error) {
         // handle error
         console.log(error);
      })
      ;
   }
}
</script>

<style lang="scss" scoped>

</style>