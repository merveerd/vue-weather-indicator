<template>
  <div id="highlights">
    <p>Weather Highlights:</p>
    {{ highlights }}
    <uv-index :highlights="highlights"></uv-index>  <!-- in other way; <uv-index :uvindex="uvindex"></uv-index> --> 
    <visibility :highlights="highlights"></visibility>
    <wind-status :highlights="highlights"></wind-status>  
  </div>
</template>

<script>
import UVIndex from './UVIndex.vue';
import Visibility from './Visibility.vue';
import WindStatus from './WindStatus.vue';

export default {
  props: ["highlights"], //as the highlights once is defined in parent(1. level), no need to define again in the return of data for 3. level components(grandchildren)
  components: { //we defined what are gonna be rendered:
    'uv-index': UVIndex,
    'visibility': Visibility,
    'wind-status': WindStatus,
  },  
  data () {
    return {
// in other way; uvindex : this.highlights.uvindex
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