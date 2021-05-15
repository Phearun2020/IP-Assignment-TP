<template>
  <div class="app">
    <h2 class="fw-bold">I am the root component</h2>
    <div class="content">
      <shape name="Diamond" color="Aquamarine"/>
      <shape name="Hexagone" color="yellow"/>
      <shape name="Star" color="pink"/>
      <shape name="Heart" color="red"/>
      <shape name="Traingle" color="BlueViolet"/>
    </div>
  </div>

</template>

<script>
import Shape from './components/Shape.vue'
export default {
  title:'Shape App',
  name: 'App',
  data(){
    return{
      todos:[],
      task:"",
    }
  },
  components:{
    Shape
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
  width: 100%;
  display: flex;
  justify-content: center;
}
body{
  
  height: 100%;
  width: 100%;

}
.app{
  background: LightSkyBlue;
  border: 3px solid black;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 700px;
  width: 800px;
}
.content{
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
}
</style>