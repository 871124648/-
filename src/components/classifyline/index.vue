<template>
  <div class="classifyline">
    <div class="flex_pro">
      <div style="width:450rpx;">
        <van-tabs :active="active" @change="onChange" :border="false" swipe-threshold="5"	>
          <van-tab title="最新"></van-tab>
          <van-tab title="最热"></van-tab>
          <van-tab title="风趣"></van-tab>
          <van-tab title="标签"></van-tab>
          <van-tab title="标签"></van-tab>
        </van-tabs>
      </div>
      <div class="ify-pro-right">

      </div>
    </div>
  </div>
</template>

<script>
export default {
   data(){
    return {
      active:null
    }
  },
  methods:{
   onChange(e){
     console.log(e.mp.detail.index);
     console.log(this.active);
   }
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.classifyline{
  width:100%;
  background:white;
  margin-top:20rpx;
}
.flex_pro{
  padding:0 16px;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.ify-pro-right{
  width:14%;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
</style>
