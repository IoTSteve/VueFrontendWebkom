
<template>

 

<div class="Plan">
  <h1>{{ msg }}</h1>
  <Dropdown></Dropdown>
  <List></List>
  {{loadedData}}
  
    
  
  
</div>
</template>

<script>
import Dropdown from '../components/Dropdown.vue'
import List from '../components/List.vue'
import axios from 'axios'

  export default {
    name: 'Plan',
    components:{
      Dropdown, List

    },
    props: {
      msg: String
    },
    data: function() {
      return {
        loadedData: "no data loaded",

      }
    },
    mounted() {
      axios.get("http://localhost:3000/mensa/Di")
      .then(response =>{
        this.loadedData = response

      })
      .catch(err =>{
        console.log(err)

      })
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>