// vuetify toolbar component 

<template>
  <v-toolbar class="tool">
    <v-toolbar-title>
      <nuxt-link class="title" to="/">Home</nuxt-link>
    </v-toolbar-title>
    <v-spacer></v-spacer>
      <nuxt-link class="nav-link nav-item title" to="/accordion">Accordion</nuxt-link>
      <nuxt-link class="nav-link nav-item title" to="/image">Image</nuxt-link>
      <nuxt-link class="nav-link nav-item title" to="/grid">Grid</nuxt-link>
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

.nav-link {
  padding-left: 2.5rem;
  font-size: 1.5rem;
}

</style>
