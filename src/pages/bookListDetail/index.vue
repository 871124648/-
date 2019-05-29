<template>
  <div class="bookListDetail">
    <div class="detail_top_pro">
      <P class="p_title" style="font-size:32rpx;margin-bottom:38rpx;">鸡鸭鱼肉样样都有（爽文直男文）</P>
      <div class="flex_pro">
          <img src="/static/icon/error.png" alt="">
          <div class="txt_pro">
            <p style="margin-bottom:14rpx;">白色黑裤衩</p>
            <span>共9本 · 宠文 · 29993点击 </span>
          </div>
          <div class="btn_pro">
            <span>5部书单</span>
          </div>
      </div>
      <div class="tap_pro">
        <van-button type="default" round size="small" style="margin-right:20rpx;">逆袭</van-button>
        <van-button type="default" round size="small" style="margin-right:20rpx;">神经女主</van-button>
        <van-button type="default" round size="small" style="margin-right:20rpx;">神经冰</van-button>
      </div>
      <p style="padding:30rpx 0rpx;color:#323237;">&nbsp;&nbsp; 一本好书足以让人忘记困意，忘记饥饿，当日也颠倒，我们则变成睁大双眼的圆脸胖鸡，看书之余，总有那些经典的好书从头到尾翻阅不止一次，看书之余这个地放根据内容适应高度高度高度高度高度高度...</p>
    </div>
    <div class="margin_bottom20"></div>
    <div v-for="item in 5" :key="item">
      <DetailProRate></DetailProRate>
      <div class="margin_bottom20"></div>
    </div>
  </div>
</template>

<script>
import DetailProRate from '@/components/DetailProRate'
export default {
    data(){
    return {
      active:2
    }
  },
  components:{DetailProRate},
  onShow(){

    },
  mounted() {

  },
  methods:{

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.detail_top_pro{
  padding:40rpx;
  background:white;
}
.flex_pro{
  display: flex;
  align-items: center;
}
.detail_top_pro>.flex_pro>img{
  width:80rpx;
  height:80rpx;
  margin-right:30rpx;
  border-radius: 50%;
}
.txt_pro{
  width:460rpx;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
.txt_pro p{
  font-size:28rpx;
  color:#323237;
  font-weight:bold;
}
.btn_pro{
  width:124rpx;
  height:60rpx;
  line-height:60rpx;
  color:#929297;
  text-align: center;
  background:rgba(245,245,247,1);
}
.tap_pro{
  padding:30rpx 0rpx;
  border-bottom:1px solid #F6F6F6;
}
.margin_bottom20{
  height:20rpx;
  background:rgba(242,242,247,1);
}



</style>
