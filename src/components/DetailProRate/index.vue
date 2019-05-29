<template>
  <div class="DetailProRate">
    <div class="flex_pro_column">
      <div class="flex_pro">
        <div style="margin-right:30rpx;">
          <img src="/static/icon/error.png" alt="">
        </div>
        <div class="flex_pro_column">
          <p class="p_title">怒江</p>
          <div><span> 连载145万字 · 102次点击 · 923人推荐</span></div>
          <div class="rate_pro">
            <div style="margin-right:30rpx;">8.9</div>
            <van-rate :value="rateValue" disabled disabled-color="#ffd21e" size="15" style="margin-top:4rpx;"/>
          </div>
        </div>
      </div>
      <div style="margin:40rpx 0;">
        <p class="p_hiden">天知道他刷了多久的副本才打下今日的江山，吾爱美人更爱自己 谁人不知红颜媚，一剑挑的珠帘翠。好了，不吹牛逼了，本来我 以为只要我</p>
      </div>
      <div class="flex_between">
        <div class="flex">
          <van-icon name="plus" size="24rpx" style="margin-right:10rpx;"/>
          <span style="margin-top:-4rpx;">加入书架</span>
        </div>
        <div>201819次点击</div>
      </div>
    </div>
  </div>
</template> 

<script>
export default {
   data(){
    return {
      rateValue:3
    }
  },
  methods:{

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.DetailProRate{
  background:white;
  padding:40rpx 30rpx;
  margin:0rpx auto;
}
.flex_pro{
  display: flex;
}
.flex_pro_column{
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
.DetailProRate .flex_pro img{
  width:104rpx;
  height:144rpx;
}
.flex,.rate_pro{
  display:flex;
  align-items: center;
}
.flex_between{
  display:flex;
  justify-content: space-between;
  }
.rate_pro{
  width:400rpx;
}
.rate_pro div{
  font-size:34rpx;
  font-weight:900;
  margin-top:-4rpx;
}
.p_hiden{
    color:#323237;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}
</style>
