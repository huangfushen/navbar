<template>
  <div class="tab-bar-item" @click="itemClick()">
    <div v-if="!isActive"> <slot name="item-icon"></slot></div>
   <div v-else > <slot name="item-icon-active"></slot></div>
   <div :style="activeStyle"> <slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name:"TabbarItem",
  props:{
    path:String,
    actvieColor:{
      type:String,
      default:'rgb(13, 183, 235)'
    }
  },
  data () {
    return {
    } 
  },
  computed: {
    isActive(){
      return this.$route.path.indexOf(this.path)!==-1
    },
    activeStyle(){
      return this.isActive ? {color:this.actvieColor} : {}
    }
  },
  methods:{
    itemClick(){
        this.$router.push(this.path)
    }
  },
  components: {

  }
}
</script>

<style>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
  padding-top: 3px;
}

</style>
