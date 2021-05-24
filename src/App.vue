<template>
  <div id="app">
    <Header />
    <Loading v-if="loading === true"/>
    <div v-else
    class="container">

    <div class="row">
    <Disco 
    v-for="(disco, index) in dischi"
    :key ="index"
    :disco = "disco"
    />

    </div>
    </div>
  </div>
</template>

<script>
/* importo per prima cosa axios */
import axios from 'axios';
/* importo il singolo disco */
import Disco from '@/components/Disco.vue'
/* importo l'header */
import Header from '@/components/Header.vue'
/* importo il caricamento */
import Loading from '@/components/Loading'

export default {
  name: 'App',
  components: {

    Disco,
    Header,
    Loading

  },
  data(){

    return{
    axios,    //inizializzo il dato axios
    dischi:[], //array che conterrò gli oggetti disco
    loading:true //flag che mi serve per il "caricamento" fin quanto axios non mi passa tutti i dati che mi servono con il get
    }

  },
  created(){

    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then(res=>{
      /* console.log(res); */
      /* console.log(res.data); */
      /* console.log(res.data.response); */
      this.dischi = res.data.response; //se il collegamento va a buon fine assegno a dischi array di oggetti il data che conterrà l'array di oggetti che mi serve
      
      this.loading = false; //imposto la variabile flag del loading a false perchè ho ricevuto i dati e quindi il caricamento deve finire
      console.log(this.dischi)

    })
    .catch(err=>{

      console.log(err); /* se il collegamento non va a buon fine allora mostrerò in console l'errore */

    })
  }
}

</script>

<style lang="scss" >
@import '@/assets/scss/general';
</style>
