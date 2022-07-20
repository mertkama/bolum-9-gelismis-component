<template>
  <div>
    <h1>Yeni Anı Componenti....</h1>
    <button @click="counter++"> Arttır!!!</button>
    <p> {{ counter }}</p>
  </div>
</template>
<script>
  export default {
    data : function(){
        return {
            counter : 0
        }
    },
    destroyed(){
        console.log("Destroyed!!!");
    },
    activated(){
        console.log("Activated!!!")
    },
    deactivated(){
        console.log("DeActivated!!!")
    }
  }
</script>

