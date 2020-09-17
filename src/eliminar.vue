<template>
  <div id="app">
    <a href="#" @click.stop="eliminar(id)"><i class="fas fa-trash-alt"></i></a>
  </div>
</template>

<script>
  export default {
    name: "eliminar",
    data() {
      return {
        message: ""
      };
    },
    methods:{
        eliminar(id){
            alert(id)
        }
    },
    mounted:function(){
       // this.count()
    }
  }

</script>

<style scoped>
#app{
    display: inline-block;
    margin-left:20px;
}
a:hover{
    color: black;
}
a{
    color:grey
}
i{
    font-size:15px;
}
</style>
