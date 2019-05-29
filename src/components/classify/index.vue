<template>
  <div class="classify">
    <van-search v-model="value" shape="round" placeholder="大铁棍子医院，找铜主任" @focus="inputFocus" />
    <div class="flex_pro">
      <div style="width:270rpx;">
        <van-tabs :active="active" @change="onChange" :border="false">
          <van-tab title="精选"></van-tab>
          <van-tab title="男生"></van-tab>
          <van-tab title="女生"></van-tab>
        </van-tabs>
      </div>
      <div class="ify-pro-right" @click="sortClick">
        <van-icon name="apps-o" size="18px" style="margin-top:4px;"/>
        <span>分类</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
   data(){
    return {
      value:'',
      active:null
    }
  },
  methods:{
   onChange(e){
     console.log(e.mp.detail.index);
     console.log(this.active);
   },
   inputFocus(){
     var url = '../searchIndex/main'
     mpvue.navigateTo({ url })
   },
   sortClick(){
     var url = '../bookSortIndex/main'
     mpvue.navigateTo({ url })
   }
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.classify{
  width:100%;
  background:white;
}
.flex_pro{
  padding:0 16px;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.ify-pro-right{
  width:90rpx;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
</style>
