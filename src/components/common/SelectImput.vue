<template>
  <div>
     <label for="cars">Choose a genre:</label>

      <select name="album" id="genere" v-model="select.value">
        <option value="All">All</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option> 
      </select>
  </div>
</template>

<script>
import select from '../shared/select'
export default {
  name: 'SelectImput',
  data(){
    return{
      select
    };
  },
  
  
}
</script>

<style lang="scss" scoped>

</style>