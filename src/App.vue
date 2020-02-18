<template>
  <div id="app"> 
    <button @click="changeLan" >switch language</button>
    <Page :lan='language' :name='stockName'/>
  </div>
</template>

<script>
import Page from './components/Page.vue'

export default {
  name: 'App',
  components: {
    Page
  },
  data:function(){
    return{
      language:'ch',
      stockName:'矽格'
    }
  },
  methods:{
    changeLan:function(){      
      this.language == 'ch'? this.language='en': this.language='ch'
    }

  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
