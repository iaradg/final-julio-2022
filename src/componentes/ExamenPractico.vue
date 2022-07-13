<template >

  <section class="src-componentes-examen-practico">
    <h4><u> Examen Final Dominguez Gordon Iara</u></h4>

      <label> Color:  </label>
          <input type="text" v-model="colorTexto">
      <label> Fondo:  </label>
          <input type="text" v-model="fondo">
      <label> Tamaño :  </label>
          <input type="text" v-model="sizeTexto">  
    <hr>
    <br>

      <label>  Texto :  </label>           
          <input  v-model.trim="textoIngresado" type="text"  :style=" {'background-color':fondo||'white','color': colorTexto, 'font-size': sizeTexto  + 'px', 'border-radius': '10px'}"> 
         
      <label>  Cantidad de Palabras : {{ textoIngresado +'   '+  contarPalabras() }} </label>           
          
      
    <hr>
    <br>   
    <hr>
    <br>
  
    <table>
        <tr>
        <th>Numero de Pregunta</th>
        <th>Respuesta</th>
        </tr>
        <tr v-for="(preg,index) in preguntas" :key="index" >
        <td>{{preg.numero}}</td>
        <td>{{preg.respuestas}}</td>
       </tr>
    </table>
 

  </section>

</template>

<script >

  export default  {
    name: 'src-componentes-examen-practico',
    props: [],
    mounted () {

    },
    data () {
      return {
        colorTexto:"",
        fondo:"",
        sizeTexto:"",
        cantPalabras:0,
        textoIngresado:"",
        preguntas : [
            { numero: 1, respuestas: ["B"] },
            { numero: 2, respuestas: ["C"] },
            { numero: 3, respuestas: ["B"] },
            { numero: 4, respuestas: ["D"] },
            { numero: 5, respuestas: ["D"] },   

            
        ]
      }
    },
    methods: {
      contarPalabras(){
        
        if(this.textoIngresado==""){
        return 0
        } else{

        let  textoDividido=this.textoIngresado.split(" ");
        let cantPalabras= textoDividido.length;
        return cantPalabras 
        }

    },
    },
    computed: {
      
    }
}


</script>

<style scoped lang="css">
  .src-componentes-examen-practico {
 color:rgb(0, 0, 0);
}
  table {
    border-collapse: collapse;
    width: 60%;
    font-size: 20px;
    background-color: rgb(255, 184, 20);
    
  }
  
  td, th {
    border: 3px solid rgb(0, 0, 0);
    text-align: left;
    padding: 8px;
  }
  
</style>
