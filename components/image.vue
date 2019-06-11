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