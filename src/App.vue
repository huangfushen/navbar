<template>
  <div id="app">
    <tab-bar>
      <tab-bar-item>
        <img slot="item-icon" src="./assets/img/home.png" />
        <div slot="item-text">首页</div>
      </tab-bar-item>
       <tab-bar-item>
        <img slot="item-icon" src="./assets/img/category.png" />
        <div slot="item-text">分类</div>
      </tab-bar-item>
       <tab-bar-item>
        <img slot="item-icon" src="./assets/img/shopcat.png" />
        <div slot="item-text">购物车</div>
      </tab-bar-item>
       <tab-bar-item>
        <img slot="item-icon" src="./assets/img/profile.png" />
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from './components/tabbar/tabbar';
import TabBarItem from './components/tabbar/tabbraItem';
export default {
  name: "App",
  components: {
    TabBar,
    TabBarItem
  }
}
</script>
<style >
@import "./assets/css/base.css";
</style>
