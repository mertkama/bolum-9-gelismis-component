<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">

        <br><br>
        <button @click="selectedComponent ='appMemory'" class="btn-sm btn btn-primary">appMemory</button>
        <button @click="selectedComponent ='appNewMemory'" class="btn-sm btn btn-primary">appNewMemory</button>
        <button @click="selectedComponent ='appAuthor'" class="btn-sm btn btn-primary">appAuthor</button>
        <hr>
        <p> {{ selectedComponent }}</p>
        <hr>

        <keep-alive>
          <component :is="selectedComponent">
          <h1 slot="heading">Güzel bir gün...</h1>
          <p>Bu çok güzel bir anıydı..</p>
        </component>
        </keep-alive>
        <!-- <app-memory slot="heading">
            <h1 slot="heading">Güzel bir gün...</h1>
            <p>Bu çok güzel bir anıydı..</p>
        </app-memory> -->
      </div>
    </div>
  </div>
</template>

<script>
  import Memory from "./components/Memory";
  import NewMemory from "./components/NewMemory";
  import Author from "./components/Author";

  export default {
    data : function(){
      return {
        selectedComponent : "appMemory"
      }
    },
    components : {
      appMemory : Memory,
      appNewMemory : NewMemory,
      appAuthor : Author
    }
  }
</script>
