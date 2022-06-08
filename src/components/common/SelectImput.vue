<template>
  <div>
     <label for="cars">Choose a genre:</label>

      <select name="album" id="genere" @change="select.value">
        <option value="">All</option>
        <option v-for="(option, index) in select.option" :key="index" value="option">
        {{option}}
        </option>
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