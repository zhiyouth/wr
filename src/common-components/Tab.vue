<template>
  <div class="wr-tab">
    <ul class="wr-tab-header">
        <li :class="'wr-tab-header-tab tab-' + index" v-for="(item, index) in data">
            
        </li>
    </ul>
  </div>
</template>

<script>/*  */
export default {
  name: 'HelloWorld',
  props: ['data', 'renderContent'],
  data () {
      return {};
  },
  created() {
      console.log('-----------------------------------', this.data)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wr-tab {
    &-header {
        
    }
}
</style>
