<template>
  <div class="hello">
    <p>hola mundo
    </p>


    <div v-for="post in APIData" :key="post.name">
    
    <p>{{ post.name }}</p>
    </div>
  </div>
</template>

<script>
import { getAPI } from '@/axios-api'


export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

  data(){
      return{
        APIData:[]
      }
    },
    created(){
      getAPI.get('/first_app/inicio',).then(response=>{
        console.log('post API has received data')
        this.APIData=response.data


      }).catch(err=>{
        console.log(err)
      })
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
