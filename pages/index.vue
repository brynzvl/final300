<template>
  <div class="app-container">
      <h1 class="hero">DISCOVER MORE MUSIC</h1>
      <br/>

      <p class="instructions">Enter an artists or album name to find their discography.</p>
      <form @submit.prevent="submit">
        <input id="search_input" placeholder="Enter an Artist or Album Name"
        v-model="search" autofocus  />

      </form>


  </div>
</template>

<script>

export default {
  components: {
  },
  data() {
    return {
      search: ''
    }
  },
  methods: {
      submit(event) {
        this.$router.push(`results/${this.search}`);
      }
  }
}
</script>

<style>
* {
  text-align: center;
}


h1 {
  padding: 2rem 0;
  font-size: 2rem;
}

#search_input {
  /* Artist Name: */
  min-width: 400px;
  font-family: WorkSans-Medium;
  font-size: 12px;
  letter-spacing: 0;
  color: #98FFBD;
  text-align: center;
  font-size: 1.5rem;
  line-height: 3rem;
  border-radius: 6px;
  border: 2px solid #98FFBD;
  
}
::placeholder {
  color: white;
  opacity: .5; /* Firefox */
}

:-ms-input-placeholder { /* Internet Explorer 10-11 */
 color: white;
}

::-ms-input-placeholder { /* Microsoft Edge */
 color: white;
}
.hero {
  /* FIND YOUR SOUND: */
  font-family: WorkSans-ExtraBold;
  font-size: 64px;
  color: #98FFBD;
  letter-spacing: 5px;
  text-align: center;
}

.instructions {
  /* Enter an artists nam: */
  font-family: WorkSans-Medium;
  font-size: 18px;
  color: #FFFFFF;
  letter-spacing: 0;
  text-align: center;
  padding-bottom: 1rem;
}

.app-container {
  padding-top: 6rem;
}

.title:visited{
  font: 700;
  color: #98FFBD;
}

.title {
  text-decoration: none;
}

</style>
