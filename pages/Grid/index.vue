<template>
    <div>
        <div class="container">
    <div class="row" >
        <div class="col-12 col-md-8"><b-img src="../../static/img/bridge.jpg" class="img-fluid " alt="Responsive image"></b-img></div>
        <div class="col-6 col-md-4"><b-img src="../../static/img/bridge.jpg" class="img-fluid " alt="Responsive image"></b-img></div>
    </div>

    <!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop -->
    <div class="row">
        <div class="col-6 col-md-4" v-for="image in images2" v-bind:key="image.alt">
    <!-- bootstrap component image -->
            <b-img v-bind:src="image.path" class="img-fluid " v-bind:alt="image.alt"></b-img>
        </div>
    </div>

    <!-- Columns are always 50% wide, on mobile and desktop -->
    <div class="row">
        <!-- bootstrap component image -->
        <div v-for="image in images3" v-bind:key="image.alt" class="col-6">
            <!-- bootstrap component image -->
            <b-img v-bind:src="image.path" class="img-fluid" v-bind:alt="image.alt"></b-img>
        </div>
    </div>
    </div>
    </div>
</template>


<script>
  export default {
    data() {
      return {  
		    images1: [
                {path: require("../../static/img/traffic.jpg"), alt:"Traffic"}, 
                {path: require("../../static/img/bridge.jpg"), alt:"Bridge"},  
            ],
            
            images2: [
                {path: require("../../static/img/tunnel.jpg"), alt:"Tunnel"}, 
                {path: require("../../static/img/coast.jpg"), alt:"Coast"}, 
                {path: require("../../static/img/sky.jpg"), alt:"Sky"}, 
            ],

            images3: [ 
                {path: require("../../static/img/traffic.jpg"), alt:"Traffic"}, 
                {path: require("../../static/img/rails.jpg"), alt:"Rails"}, 
            ]
    }
  }
  }
</script>