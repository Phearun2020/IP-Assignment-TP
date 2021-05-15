<template>
  <div id="app">
      <h3>I'm the root component</h3>
  <div class="row">
    <div id="triangle">
    </div>
    <div id="hexagon">
      <div id="heart"></div>
    </div>
    <div id="heart"></div>
    <div id="cut-diamond">
      <div id="star-five"></div>
    </div>
    <div id="star-five"></div>
  </div>
  

</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#app {
  height: 600px;
  width: 800px;
  background-color: rgb(123, 202, 238);
  
  border: 2px solid black;
}
h3{
  margin: 20px;
}
#triangle{
  margin-left: 40px;
  width: 0;
  height: 0;
  border-left: 70px solid transparent;
  border-right: 70px solid transparent;
  border-bottom: 100px solid red;
}
#hexagon {
  width: 100px;
  height: 57.735px;
  background: red;
  position: relative;
}
#hexagon::before {
  content: "";
  position: absolute;
  top: -28.8675px;
  left: 0;
  width: 0;
  height: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-bottom: 28.8675px solid red;
}
#hexagon::after {
  content: "";
  position: absolute;
  bottom: -28.8675px;
  left: 0;
  width: 0;
  height: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-top: 28.8675px solid red;
}
#heart {
      position: relative;
      width: 100px;
      height: 90px;
    }
    #heart:before,
    #heart:after {
      position: absolute;
      content: "";
      left: 50px;
      top: 0;
      width: 50px;
      height: 80px;
      background:beige;
      border-radius: 50px 50px 0 0;
      transform: rotate(-45deg);
      transform-origin: 0 100%;
    }
    #heart:after {
      left: 0;
      transform: rotate(45deg);
      transform-origin: 100% 100%;
    }

    #cut-diamond {
      border-style: solid;
      border-color: transparent transparent red transparent;
      border-width: 0 25px 25px 25px;
      height: 0;
      width: 50px;
      box-sizing: content-box;
      position: relative;
      margin: 20px 0 50px 0;
    }
    #cut-diamond:after {
      content: "";
      position: absolute;
      top: 25px;
      left: -25px;
      width: 0;
      height: 0;
      border-style: solid;
      border-color: red transparent transparent transparent;
      border-width: 70px 50px 0 50px;
    }

    #star-five {
      margin: 50px 0;
      position: relative;
      display: block;
      color: red;
      width: 0px;
      height: 0px;
      border-right: 100px solid transparent;
      border-bottom: 70px solid red;
      border-left: 100px solid transparent;
      transform: rotate(35deg);
    }
    #star-five:before {
      border-bottom: 80px solid red;
      border-left: 30px solid transparent;
      border-right: 30px solid transparent;
      position: absolute;
      height: 0;
      width: 0;
      top: -45px;
      left: -65px;
      display: block;
      content: '';
      transform: rotate(-35deg);
    }
    #star-five:after {
      position: absolute;
      display: block;
      color: red;
      top: 3px;
      left: -105px;
      width: 0px;
      height: 0px;
      border-right: 100px solid transparent;
      border-bottom: 70px solid red;
      border-left: 100px solid transparent;
      transform: rotate(-70deg);
      content: '';
    }
  
    
    
  
</style>
