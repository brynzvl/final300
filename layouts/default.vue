<template>
  <section>
    <ToolBar/>
    <nuxt class="app-body"/>
    </section>
</template>

<script>
import ToolBar from '~/components/Toolbar.vue';

export default {
  components: {
    ToolBar
  },

  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style>
  .app-body {
    /* Rectangle: */
    background-image: linear-gradient(-180deg, #0B84A9 0%, #054C70 100%);
    min-height: 100vh;
      font-family: WorkSans-Medium;

  }

    .album-container {

    display: grid;
    max-width: 9000px;
    margin: auto;
    padding: 1rem;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    grid-gap: 1rem;
  }
  .card {
    display: grid;
    min-width: 180px;
    max-width: 1fr;
    background-color: white;
  }

  .album {
  font-family: WorkSans-Medium;
  font-size: 28px;
  color: #98FFBD;
  letter-spacing: 0;
  line-height: 32px;
  text-align: left;

  }
  
  .artist {
    padding-top: .5rem;
    font-family: WorkSans-Medium;
    font-size: 20px;
    color: #FFFFFF;
    letter-spacing: 0;
    text-align: left;

  }

  .title:visited{
  font: 700;
  color: #98FFBD;
}

  .album-art {
  height: 100px;
  max-width: 130px;
  margin: 0; }

</style>