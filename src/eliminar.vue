<template>
  <div id="app">

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
          borrar(id){
               this.$emit("borrar",{id:id})
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
