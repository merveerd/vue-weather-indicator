<template>
  <div id="app">
 <p>This component’s code is in {{ filename }}</p>
<Content v-bind:weather_data="weather_data"></Content>  
 </div>
</template>

<script>
import Content from './components/Content.vue'
export default {
  name: 'app',
  components: {
    'Content': Content // 'Content' is template component name, Content is imported component
  },
  data () {
    return{
filename : 'App.vue',
// this is where you define your props to be sent. Yani bir prop gondereceksen data nin returninde tanimlamalisin
weather_data: { // when you binding in template, do not give any whitespace between v-bind: and weather_data 
        location: "California",
        temperature: {
          current: "35 C",
        },
        highlights: {
          uvindex: "3",
          windstatus: {
            speed: "20 km/h",
            direction: "N-E",
          },
          visibility: "12 km",
        },
      },

    }
  },
  methods: {

  },
  computed: {

  },
    
}
</script>

<style>
</style>
