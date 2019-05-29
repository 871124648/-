<template>
  <div class="readDetail" :class="blackShow?'backgroundBlack':''">
      <div v-if="show">
        <sectionpage></sectionpage>
      </div>
      <p class="p_title" style="font-size:36rpx;margin-bottom:40rpx;" :class="blackShow?'backgroundBlack':''">第一百八十四章 &nbsp;&nbsp; 你是不是有病 </p>
      <div @click="editClick">
        <p>2014年，华共国，魔都。六月的教养炙烤着大地，仿佛要蒸干好多 沥青路上最后一丝水汽。</p>
        <p>墨艺术个肯呢个萨里哦券妈妈你其诶情况 阿迪穷奇葩大佛爱富婆爱的彷佛爱的奥看了， 飞机啊考虑到积分卡海景。的境况很卡的非卡</p>
        <p>阿打发打发ad覅ad覅打翻了金球奖大了， 大佛脾气皮跑脾气漆器IEUR去乌尔u苏打粉怕 阿迪破气魄IQ破IPOis破if</p>
        <p>“打发爱的发的ad覅啊”评为问道。</p>
        <p>“哦否去我去偶偶一is对哦复习下哦手机 爱打飞机啊哦哦”评为问道。</p>
        <p>阿打发打发ad覅ad覅打翻了金球奖大了， 大佛脾气皮跑脾气漆器IEUR去乌尔u苏打粉怕 阿迪破气魄IQ破IPOis破if 拷贝</p>      
        <p>2014年，华共国，魔都。六月的教养炙烤着大地，仿佛要蒸干好多 沥青路上最后一丝水汽。</p>
        <p>墨艺术个肯呢个萨里哦券妈妈你其诶情况 阿迪穷奇葩大佛爱富婆爱的彷佛爱的奥看了， 飞机啊考虑到积分卡海景。的境况很卡的非卡</p>
        <p>阿打发打发ad覅ad覅打翻了金球奖大了， 大佛脾气皮跑脾气漆器IEUR去乌尔u苏打粉怕 阿迪破气魄IQ破IPOis破if</p>
        <p>“打发爱的发的ad覅啊”评为问道。</p>
        <p>“哦否去我去偶偶一is对哦复习下哦手机 爱打飞机啊哦哦”评为问道。</p>
        <p>阿打发打发ad覅ad覅打翻了金球奖大了， 大佛脾气皮跑脾气漆器IEUR去乌尔u苏打粉怕 阿迪破气魄IQ破IPOis破if 拷贝</p>            
      </div>
      <div v-if="bottomShow" class="bottom_fixed">
        <editComponent @tabClick="tabClick" @popupClick="popupClick" @rechargeClick="rechargeClick"></editComponent>
      </div>
      <div v-if="blackShow" class="bottom_fixed">
          <editBlackComponent @whiteClick="whiteClick" @popupClick="popupClick" @rechargeClick="rechargeClick"></editBlackComponent>
      </div>
      <van-popup :show="popupShow" position="left" overlay="true" @close="onClose">
        <div style="font-size:28rpx;">
          <div class="top_title">章节目录 · 正文</div>
          <div class="content_pro">
            <div v-for="item in 15" :key="item">第一章 &nbsp;&nbsp;&nbsp; 少年不知愁滋味</div>
          </div>
        </div>
      </van-popup>
      <div v-if="rechargeShow" class="bottom_fixed">
        <recharge :isblack="blackShow?true:false"></recharge>
      </div>
  </div>
</template>

<script>
import sectionpage from '@/components/sectionpage'
import editComponent from '@/components/editComponent'
import editBlackComponent from '@/components/editBlackComponent'
import recharge from '@/components/recharge'

export default {
  config: {
    "enablePullDownRefresh": true,
  },
  async onPullDownRefresh() {
    this.show = true;
    this.bottomShow = false;
    wx.stopPullDownRefresh();
  },
  data(){
    return {
      show:false,
      bottomShow:false,
      blackShow:false,
      popupShow:false,
      rechargeShow:false
    }
  },
  components:{sectionpage,editComponent,editBlackComponent,recharge},
  onShow(){

    },
  mounted(){

  },
  methods:{
    editClick(){
      this.show = false;
      this.rechargeShow = false;
      this.bottomShow = true;
    },
    tabClick(val){
      this.blackShow = true;
      this.bottomShow = false;
    },
    whiteClick(){
      this.blackShow = false;
      this.bottomShow = true;
    },
    onClose(){
      this.popupShow = false;
    },
    popupClick(){
      this.popupShow = true;
    },
    rechargeClick(){
      this.rechargeShow = true;
      this.bottomShow = false;
    }
  }
}
</script>

<style>
@import "../../app.wxss";
.readDetail{
  padding:76rpx 40rpx;
  color:rgba(50,50,55,1);
}
.readDetail>div>p{
  text-indent: 60rpx;
  font-size:34rpx;
  line-height:60rpx;
  font-weight:400;
  font-family:'MicrosoftYaHei';
}
.bottom_fixed{
  position:fixed;
  bottom:0;
  left:0;
}
.backgroundBlack{
  background:#333333;
  color:#F7F7F7;
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
page{
  background:#F5F5F7;
}
</style>
