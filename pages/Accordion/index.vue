

<template>

  <div>
    <b-card no-body class="mb-1" v-for="data in accordionData" v-bind:key="data.title">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block href="#" v-b-toggle.accordion-1 variant="info">{{data.title}}</b-button>
      </b-card-header>
      <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-card-text>{{ data.text }}</b-card-text>
        </b-card-body>
      </b-collapse>
    </b-card>
 </div>
</template>

<script>
  export default {
    data() {
      return {  
		    accordionData: [
    	        { title: 'CASE STUDY / PERSONAL', text: 'Using machine learning to create a better color tool for designers.' },
                { title: 'PROJECT / PROFESSIONAL', text: 'Helping New Yorkers become more flood resilient.' },
                { title: 'PROJECT / PROFESSIONAL', text: 'Prototyping a behavior change app to help people quit smoking.' }
            ]
       }
    }
  }
</script>