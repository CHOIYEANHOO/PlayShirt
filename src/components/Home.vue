<template>
   <div id="app">
       <ComHeader></ComHeader>
   </div>
</template>

<script>
import Vue from 'vue'
import ComHeader from '../public/ComHeader.vue'
import ComFooter from '../public/ComFooter.vue'

export default {
  name: 'Home',
  data () {
    return {}
  },
  components:{
    ComHeader,
    ComFooter
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
