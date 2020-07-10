.<template>
  <div class="wrap">
    <div id="miApp">
        <h3>Hola, {{ nombre }} aprenderá:</h3>
        <div>
            <p v-if="mostrar_titulo_lista"><b>{{titulo_lista}}</b></p>
            <p v-else><b>{{titulo_else}}</b></p>
            <ul>
               <li v-for="(lenguaje, i) in lenguajes" v-bind:key="i">{{lenguaje}}</li>
            </ul>
        </div>
    </div>
    
   
  </div>
</template>

<script>
export default {
    name: 'MiLista',
    props: {
        msg: String
    },
    data: function(){
        return{
            nombre: "Michelle",
            titulo_lista: "Lenguajes:",
            titulo_else: "Aprendí Todo",
            mostrar_titulo_lista: true,
            lenguajes: ['HTML', 'CSS', 'Vue','Firebase', 'Python', 'Dart']
        }
       
    }

}
</script>

<style scoped>
    .wrap {
    margin: auto;
    height: auto;
    width: 800px;
    text-align: center;
    border: 2px solid black;
    font-size: 25px;
    }
    ul {
        list-style: none;
    }

</style>