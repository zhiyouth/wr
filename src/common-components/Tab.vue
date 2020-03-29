<template>
  <div class="wr-tab">
    <ul class="wr-tab-header">
        <li :class="'wr-tab-header-tab tab-' + index" v-for="(item, index) in data"
          @click="tabClick(index)"
        >
            {{item.text ? item.text : null}}
        </li>
    </ul>
    <div class="wr-tab-content">
      {{this.renderContent && this.renderContent(active)}}
      <slot></slot>
    </div>
  </div>
</template>

<script>/*  */
export default {
  name: 'HelloWorld',
  props: ['data', 'renderContent'],
  data () {
      return {
        active: 0
      };
  },
  created() {
      console.log('-----------------------------------', this.renderContent)
  },
  methods: {
    tabClick(index) {
      this.active = index;
      console.log(this.active, '点击')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wr-tab {
}
.wr-tab-header {
  display: flex;
  justify-content: center;
  align-items: center;
}
.wr-tab-header-tab {
  height: 40px;
  background-color: pink;
  display: flex;
  justify-content: center;
  align-items: center;
  flex: 1;
}
</style>
