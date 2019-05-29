<template>
  <div class="beginRead">
    <div class="flex_pro">
      <div style="width:380rpx;" class="flex">
        <img src="/static/icon/fenxiang.png" alt="">
        <img src="/static/icon/zan.png" alt="">
        <img src="/static/icon/shujia.png" alt="">
      </div>
      <div>
        <button class="readBtn" @click="readBengin">开始阅读</button>
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
  mounted() {

  },
  methods:{
    readBengin(){
      //  wx.setNavigationBarTitle({
      //   title: "已修改"
      // })
      var url="../readDetail/main";
      mpvue.navigateTo({url});
    }
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.beginRead{
  background:white;
  padding:25rpx 40rpx;
  margin-top:20rpx;
}
.flex_pro{
  display: flex;
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
.beginRead>.flex_pro img{
  width:42rpx;
  height:42rpx;
  margin-right:68rpx;
}

.flex{
  display:flex;
  align-items: center;
}
.readBtn{
  font-size:28rpx;
  width:300rpx;
  height:70rpx;
  border:none;
  outline: none;
  border-radius: 50rpx;
  color:white;
  background-color: #00E2BB;
  background:linear-gradient(90deg,rgba(29,188,156,1),rgba(59,225,192,1));
}
</style>
