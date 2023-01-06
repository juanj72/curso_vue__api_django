<template>

    <h2>hola mundo desde otro component</h2>


    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Debitis ea distinctio, repellendus, expedita deleniti totam tempore error quisquam aut eaque iusto consequuntur ut neque quia doloribus velit odio quidem dignissimos!</p>
</template>

<script>

export default {
  name: 'MenuInicio',
  props: {
    msg: String
  }
}

</script>



<style scoped>
h2{
    color: aqua;
}
p{
    color: yellow;
}
</style>