<template>
  <div id="uvindex">
    <p>UV Index: {{ uvindex }}</p>
  </div>
</template>

<script>

export default {
  props: ["highlights"], // in other way;  props: ["uvindex"],
  data () {
    return {
      uvindex: this.highlights.uvindex // in other way; remove this
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