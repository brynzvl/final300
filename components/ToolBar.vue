<template>
  <v-toolbar class="tool">
    <v-toolbar-title>
      <nuxt-link class="title" to="/">Home</nuxt-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <nuxt-link class="title" to="Accordion">Accordion</nuxt-link>
  </v-toolbar>
</template>
<script>
</script>
<style scoped>
.title {
  text-decoration: none !important;
  font-family: WorkSans-Medium;

}
.title:visited{
  font: 700;
  color: #98FFBD;
}


.tool {
  box-shadow: none;
  background-color: #054D71;
    font-family: WorkSans-Medium;

 
}

</style>
