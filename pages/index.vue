<template>
<div>
  <!-- <div class="app-container"> -->
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

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.grid-container {
    max-width: 1200px;
    margin: 0 auto;
    display: grid;
    grid-template-areas:
        'header header header'
        'nav nav nav '
        'sidebar main main '
        'footer footer footer';
}

.grid-container>div {
    font-family: sans-serif;
    padding: 1rem;
}

ul {
    list-style: none;
    padding: 0;
}

li {
    list-style-type: none;
}

h1 {
    font-size: 2rem;
    line-height: 120%;
}

.header {
    grid-area: header;
}


/* .nav {
    grid-area: nav;
    display: flex;

    li{
        display: inline-flex;
        padding: 0 20px 0 0;
    }
    &:after{
        padding: 1rem;
    }
} */

.main {
    grid-area: main;

}

/* .sidebar {
    grid-area: sidebar;

    li {
        padding: 0 0 20px 0;
    }
} */

/* // .footer {
//     display: flex;
//     grid-area: footer;
//     padding-top: 1rem;

//     li {
//         display: inline;
//         padding: 0 20px 0 0;
//     }
// } */

.footer>div {
    display: flex;

}


#logo {
    width: 200px;
}

/* // .clearfix {
//     &:after {
//         padding: .5rem;
//     }
// } */

/* .header-img {
   content: url(../../img/header.jpg);
    background-size: inherit; } */

.collapse-container {
    padding: 2rem;
}

body {
    background-color: #fff;
    min-height: 100vh;
    font: normal 16px sans-serif;
}

.gallery-container h1 {
    text-align: center;
    margin-top: 70px;
    font-family: 'Droid Sans', sans-serif;
    font-weight: bold;
    color: #58595a;
}

.gallery-container p.page-description {
    text-align: center;
    margin: 30px auto;
    font-size: 18px;
    color: #85878c;
}


#logo-link {
    padding: 0;
    font-size: 1.5rem;
    font-weight: Bold;
    color: #4fc08d;

}

.nav-link {
    color: #4fc08d;
    font-size: 1.1rem;

}

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


#btn-success {
    background-color: #4fc08d;
    border-color: #4fc08d;
}


.media { 
    min-width: 0;
    margin: 5px;
    border-radius: 1rem;
}


.row>div {
    padding: 1rem;


}

img {
    border-radius: 8px;
}

</style>
