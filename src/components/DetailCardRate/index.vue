<template>
  <div class="DetailCardRate">
    <div class="flex_pro_column">
      <div class="flex_pro">
        <div style="width:190rpx;">
          <img src="/static/icon/error.png" alt="">
        </div>
        <div class="flex_pro_column">
          <p class="p_title">一怒为红颜（直男专区）</p>
          <span style="font-size:28rpx;color:#323237;">终结小猪猪&nbsp;&nbsp;玄幻</span>
          <div><span> 连载145万字 · 102次点击 · 923人推荐</span></div>
          <div class="rate_pro">
            <div>8.9</div>
            <van-rate :value="rateValue" disabled disabled-color="#ffd21e" size="15" style="margin-top:4rpx;"/>
            <span @click="tateClick" style="color:#08C6A5;">我来点评</span>
          </div>
        </div>
      </div>
      <div style="margin-top:40rpx">
        <p class="p_hiden">天知道他刷了多久的副本才打下今日的江山，吾爱美人更爱自己 谁人不知红颜媚，一剑挑的珠帘翠。好了，不吹牛逼了，本来我 以为只要我</p>
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
    tateClick(){
      var url = "../booksComment/main";
      mpvue.navigateTo({url})
    }

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.DetailCardRate{
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
.DetailCardRate .flex_pro img{
  width:160rpx;
  height:220rpx;
}
.flex,.rate_pro{
  display:flex;
  align-items: center;
}
.rate_pro{
  width:400rpx;
  justify-content: space-between;
}
.rate_pro div{
  font-size:34rpx;
  font-weight:900;
  margin-top:-4rpx;
}
.p_hiden{
     overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}
.flex_between{
  display:flex;
  justify-content: space-between;
  padding-top:20rpx;
  border-top:1px solid #EFEFEF;
  }
</style>
