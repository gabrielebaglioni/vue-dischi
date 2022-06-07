<template>
    <main>
       <SectionAlbum></SectionAlbum>
    </main>
</template>

<script>
import SectionAlbum from '../sectiones/Section-Album.vue';
export default {
    name: "BaseMain.",
    components: { SectionAlbum },
}
</script>

<style lang="scss" >
 main{
         background-color: #1E2D3B;
         
 }
  

</style>