<template>
  <div class="">
    <p class="display-title" >Displaying Results for</p>
    <h2>{{$route.params.id}}</h2>
    <div v-if="albumExists">
      <div class="album-container">
      <div v-for="(album) in albumData" v-bind:key="album.id">
        <Card
          :title="album.collectionCensoredName"
          :image="album.artworkUrl100"
          :artistName="album.artistName"
          :url="album.artistViewUrl"
        />

      </div>
      </div>
    </div>
  </div>
</template>
<script>
import axios from 'axios';
import Card from '~/components/Card.vue';
export default {
  asyncData({params}) {
    return axios.get(`https://itunes.apple.com/search?term=${params.id}&entity=album`)
      .then((response) => {
        return {albumData: response.data.results}
      });
  },
  components: {
      Card
  },
  middleware: 'search',
  methods: {
  
  },
  computed: {
    albumExists() {
      return this.albumData.length > 0;
    }

  }

}
</script>

<style>
 .display-title {
    padding-top: 3rem;
    font-family: WorkSans-Medium;
    color: white;
    letter-spacing: 0;
    text-align: center;
    font-size: 18px;
  }

  h2 {
  
    font-family: WorkSans-Medium;
    font-size: 64px;
    color: #98FFBD;
    letter-spacing: 0;
    text-align: center;
    line-height: 60px;
    padding-bottom: 3rem;

  }

  

 
</style>