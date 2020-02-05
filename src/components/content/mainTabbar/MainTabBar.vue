<template>
  <tab-bar>
    <tab-bar-item path="/home" activeColor="rgba(218, 86, 126, 0.918)">
      <!-- 因为assets定义为了别名。所以在用的时候前面要用~ -->
      <img slot="item-icon" src="~assets/img/tabbar/home.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/home_active.png" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" activeColor="rgba(218, 86, 126, 0.918)">
      <img slot="item-icon" src="~assets/img/tabbar/category.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/category_active.png" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart" activeColor="rgba(218, 86, 126, 0.918)">
      <img slot="item-icon" src="~assets/img/tabbar/shopacrt.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/shopacrt_active.png" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile" activeColor="rgba(218, 86, 126, 0.918)">
      <img slot="item-icon" src="~assets/img/tabbar/profile.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/profile_active.png" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>

import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem'

export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem
  }
}
</script>



<style scoped>

</style>