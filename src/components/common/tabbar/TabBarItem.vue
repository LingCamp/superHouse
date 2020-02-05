<template>
  <div class="tab-bar-item" @click="itemClick">
    <!-- item-icon命名这个是用来放图片的；item-text命名这个是用来放字的 -->
    <div v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>  
    </div>
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>  
    
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'rgba(218, 86, 126, 0.918)'
    }
  },
  data() {
    return {
      // isActive: true,
      // path: './home'
    }
  },
  computed: {
    isActive() {
      //判断this.$router.path这个是正在活跃的路径；this.path是props的path是否一样
      // /home -> item1(/home) = true
      // indexOf  == 1话就是找到了，意味着this.$router.path=this.path就显示
      return this.$route.path.indexOf(this.path) !== -1 
    },
    activeStyle() {
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    itemClick() {
      // console.log('itemclick');
      this.$router.replace(this.path)
    }
  }
}
</script>

<style scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;     /*  图片下面与文字之间空隙的距离  */
  margin-bottom: 2px;
}
/* .active {
  color: rgba(218, 86, 126, 0.918);
} */

</style>