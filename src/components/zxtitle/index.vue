<template>
  <div class="zxtitle">
    <div class="flex_pro">
      <div style="width:400rpx;">
        <span class="title_pro">{{title}}</span>
      </div>
      <div class="ify-pro-right">
        <van-icon name="plus" size="18px" style="margin-top:5px;"/>
        <span>查看更多</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
   data(){
    return {
    }
  },
  props:{
    title:{}
  },
  methods:{

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.zxtitle{
  background:white;
  padding:25rpx 40rpx;
  margin-top:20rpx;
}
.flex_pro{
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.ify-pro-right{
  width:140rpx;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.title_pro{
  color:#333333;
  font-size:34rpx;
  font-weight:900;
}
</style>
