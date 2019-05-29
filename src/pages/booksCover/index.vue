<template>
  <div class="booksCover">
    <div>
      <DetailCardRate></DetailCardRate>
      <div class="flex_between mulu_pro" @click="chapterClick">
        <p class="p_title">章节目录</p>
        <div class="flex">
          <span style="margin-top:-4rpx;">共1095章</span>
          <van-icon name="plus" size="24rpx" style="margin-left:10rpx;"/>
        </div>
      </div>
    </div>
    <div class="margin_bottom20"></div>
    <div class="flex select_pro">
      <div class="flex_conent">
        <img src="/static/icon/toupiao.png" alt="">
        <span>我要投票</span>
      </div>
      <span></span>
      <div class="flex_conent">
        <img src="/static/icon/user-qd.png" alt="" style="width:60rpx;height:60rpx;margin-right:16rpx;">
        <span>我要打赏</span>
      </div>
    </div>
    <div class="margin_bottom20"></div>
    <div style="padding:25rpx 40rpx;margin-bottom:40rpx;">
          <div class="flex_between">
            <p class="p_title">精彩点评</p>
            <div class="flex">
              <van-icon name="plus" size="24rpx" style="margin-right:10rpx;"/>
              <span style="margin-top:-4rpx;">更多</span>
            </div>
          </div>
          <div v-for="item in 5" :key="item" style="margin-bottom:60rpx;">
              <remarkPro></remarkPro>
          </div>
    </div>
    <div class="bottom_pro">
      <beginRead></beginRead>
    </div>
    <van-popup :show="show" position="left" overlay="true" @close="onClose">
      <div style="font-size:28rpx;">
        <div class="top_title">章节目录 · 正文</div>
        <div class="content_pro">
          <div v-for="item in 15" :key="item">第一章 &nbsp;&nbsp;&nbsp; 少年不知愁滋味</div>
        </div>
      </div>
    </van-popup>

  </div>
</template>

<script>
import DetailCardRate from '@/components/DetailCardRate'
import remarkPro from '@/components/remarkPro'
import beginRead from '@/components/beginRead'
export default {
    data(){
    return {
      active:2,
      show:false
    }
  },
  components:{DetailCardRate,remarkPro,beginRead},
  onShow(){

    },
  mounted() {

  },
  methods:{
    chapterClick(){
        this.show = true;
    },
    onClose(){
      this.show = false;
    }
  }
}
</script>

<style scoped>
.margin_bottom20{
  height:20rpx;
  background:rgba(242,242,247,1);
}
.select_pro img{
  width:82rpx;
  height:82rpx;
}
.flex{
  display: flex;
  align-items:center;
}
.flex_conent{
  display: flex;
  align-items:center;
  justify-content: center;
}

.select_pro{
  padding:20rpx;
  justify-content: space-around;
}
.select_pro>div{
  width:300rpx;
}
.select_pro>span{
  border-right:2rpx solid #F5F5F5;
  width:2rpx;
  height:60rpx;
}
.flex_between{
  display:flex;
  justify-content: space-between;
  }
.bottom_pro{
  position:fixed;
  left:0;
  bottom:0;
}
.mulu_pro{
  width:680rpx;
  padding:30rpx 0rpx;
  margin:0 auto;
  border-top:1px solid #EFEFEF;
}
.top_title{
  height:70rpx;
  line-height: 70rpx;
  color:#929297;
  padding:0 40rpx;
  background:rgba(242,242,247,1);
}
.content_pro{
  padding:40rpx;
}
.content_pro>div{
  margin-bottom:40rpx;
  color:#929297;
  font-size:28rpx;
}
</style>
