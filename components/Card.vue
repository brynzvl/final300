<template>
  <div class="card-shape">
    <v-card hover target="_blank" :href="url" :color="color" class="white--text v-card">
    <v-img :src="image" class="album-art" contain></v-img>
    </v-card>
    <div class="details">
    <div class="album">{{title}}</div>
    <div class="artist">{{artistName}}</div>
    </div>
  </div>

</template>
<script>
export default {
  props: ['title', 'image', 'artistName', 'url',]
}
</script>

<style>
  .v-card {
    /* display: inline-flex; */
    max-width: 100px;
    margin-bottom: 16px;
    
    
  }
  
  
  .album-container {
    padding-top: 2rem; 
    max-width: 1000px; 
    margin: auto;
  }

  .album {
  font-family: WorkSans-Medium;
  font-size: 24px;
  color: #ffffff;
  letter-spacing: 0;
  line-height: 22px;
  text-align: left;

  }
  
  .artist {
    font-family: WorkSans-Medium;
    font-size: 16px;
    color: #98FFBD;
    letter-spacing: 0;
    text-align: left;

  }

  .title:visited{
  font: 700;
  color: #98FFBD;
}

  .album-art {
  height: 100px;
  max-width: 100px; 

}

.card-shape {
  margin: 1rem 0 0 0;
  padding: 2rem 0 0 0;
  /* display: flex; */
}

</style>