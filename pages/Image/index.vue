<template>
<div class="app-container">
    <div class="grid-container">
         <div class="container">
             <img id="space" src="../../static/img/space.png" class="img-fluid" alt="Responsive image">
             <div class="image-box">
                <b-img v-for="image in images" v-bind:src="image.path" class="img-fluid" v-bind:key="image.alt" v-bind:alt="image.alt"> </b-img>
            </div>
         </div>
    </div>
    </div>
</template>

<script>
  export default {
    data() {
      return {  
		    images: [
                {path: require("../../static/img/traffic.jpg"), alt:"Traffic"}, 
                {path: require("../../static/img/bridge.jpg"), alt:"Bridge"}, 
                {path: require("../../static/img/tunnel.jpg"), alt:"Tunnel"}, 
                {path: require("../../static/img/coast.jpg"), alt:"Coast"}, 
                {path: require("../../static/img/sky.jpg"), alt:"Sky"}, 
                {path: require("../../static/img/rails.jpg"), alt:"Rails"}, 
            ]
       }
    }
  }
</script>


<style>
.image-box {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
.image-box img {
    width: 350px;
    max-width: 100%;
    max-height: 350px;
    margin: 8px;
    border-radius: 8px;
}

</style>