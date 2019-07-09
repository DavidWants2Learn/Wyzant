<template>
  <svg>
  </svg>
</template>

<script>
const d3 = require('d3');

export default {
  name: "app",
  data: function() {
    return {
      loadData: []
    };
  },
  mounted() {
    console.log("App loaded");
    this.fetchData();
  },
  methods: {
    async fetchData() {
      let data = await d3.json("~/data/responsetime.json");
      this.loadData = data;
    }
  },
}
</script> 

<style>
</style>