<template>
  <div class="remarkPro">
    <div class="flex top_pro">
      <img src="/static/icon/error.png" alt="">
      <span style="color:#626267;margin:0 20rpx;">谁是的新欢</span>
      <span style="margin-right:10rpx;">点评</span>
      <van-rate :value="rateValue" disabled disabled-color="#ffd21e" size="12" style="margin-top:4rpx;"/>
    </div>
    <p class="book_list_content">不错，虽然写的不怎么滴，但是感觉还是需要鼓励一下的，真的实在啊写的行云流水，但是写的真不怎么滴</p>
    <div class="flex_between">
        <div>2020-10-01 14:12</div>
        <div class="flex">
          <img src="/static/icon/zan.png" alt="">
          <!-- <img src="/static/icon/zan-on.png" alt=""> -->
          <span style="margin-left:8rpx;margin-top:4rpx;">34</span>
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
.remarkPro{
  margin-top:20rpx;
}
.flex{
  display: flex;
  align-items: center;
}
.top_pro>img{
  width:48rpx;
  height:48rpx;
  background:rgba(133,133,133,1);
  border-radius:50%;
}
.ify-pro-right{
  width:140rpx;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.book_list_content{
    color:#323237;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    margin:30rpx 0;
}
.flex{
  display: flex;
}
.flex-column{
  display: flex;
  flex-direction:column;
  justify-content:center;
}
.flex_between{
  display:flex;
  justify-content: space-between;
  align-items:center;
}
.flex_between img{
  width:30rpx;
  height:30rpx;
}
</style>
