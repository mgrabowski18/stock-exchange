<template>
  <div>
    <my-stock v-for="stock in stocks" :stock="stock"></my-stock>
  </div>
</template>
<script>
  import Stock from './Stock.vue'
  export default {
    components: {
      'myStock': Stock
    },
    computed: {
      stocks(){
        return this.$store.getters.getStocks
      }
    }
  };
</script>