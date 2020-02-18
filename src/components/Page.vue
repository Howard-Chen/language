<template>
  <div>
     <h2>{{lan_file.title}}</h2>
    <p>{{lan_file.paragraph}}</p>    
  </div>
</template>

<script>
  export default {
    name: 'Page',
    props: ['lan','name'],
    data:function(){
      return{
        lan_ch:{
          title:"股票",
          paragraph:`求求你 ${this.name} 不要跌`
        },
        lan_en:{
          title:"Stock Market",
          paragraph:`Please ${this.name} dont drop`
        },
        
      }    
    }
    ,computed:{
     lan_file:function(){        
        if(this.lan =="ch"){
          return this.lan_ch;
        }else{
          return this.lan_en;
        }
      }
    }


  }
</script>


<style scoped>

</style>
