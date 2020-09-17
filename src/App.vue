<template>
  <div id="app" class="text-center">
    <span id="titulo" class="align-bottom mr-4">Lista de tareas</span>
        <img src="src/img/lista-de-verificacion.svg">
    <div id="tarea" class="col-3-4 d-flex flex-column align-items-center mt-2">
        <h4 class="mt-2">{{message}}</h4>
        <input type="text" v-model="skill" placeholder="ingrese una nueva tarea" class="mt-2 mb-3 text-center" @keyup.enter="add_list">
        <button v-on:click=add_list class="mt-2 mb-5 btn btn-secondary btn-sm"> Crear </button>
        <h5><u>Lista</u></h5>
        <ul class="px-0">
            <li v-for="skill in skills" :key="skill.id">{{skill}}<eliminar v-bind:key="skill.id" id="skill.id"></eliminar></li>
        </ul>
    </div>
  </div>
</template>
<script>
import eliminar from "./eliminar.vue"
  export default {
    props:{
        id:Number,
        require: true,
    },
    data() {
      return {

        message: "Crea una nueva tarea",
        skills:[],
        skill:"",
    };
    },
    components:{eliminar},
    methods:{
        add_list: function () { 
            if(this.skill != ""){
            this.skills.push(this.skill)
            this.skill="";
            }
        }
    }
  }
</script>

<style scoped>

#titulo{
    color: indigo;
    font-size: 70px;
}
h4{
    color: blueviolet;
}

input{
    color:gray;
}
img{
    width: 5%;
    align-content: flex-start;
}

</style>