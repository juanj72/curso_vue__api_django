<template>
<h2>prueba de componentes en vue</h2>

<p>programacion de frontend en mi camino a un nuevo trabajo</p>
<div v-for="post in APIData" :key="post.id">
<p>{{ post.title }}</p>
<p>{{ post.content }}</p>
<hr>
</div>

</template>

<script>

import {getAPI} from '../axios-api'

  export default{
    name:'Componente_prueba',
    props:{
        msg:String
    },
    data(){
      return{
        APIData:[]
      }
    },
    created(){
      getAPI.get('/first_app/post_api2',).then(response=>{
        console.log('post API has received data')
        this.APIData=response.data


      }).catch(err=>{
        console.log(err)
      })
    }
  }
</script>