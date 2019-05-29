<template>
  <div class="bookCity">
   <classify></classify>
    <div class="width_pro">
      <swiper class="swiper" indicator-dots="true" autoplay="true" interval="5000" duration="1000">
        <block v-for="(item, index) in movies" :index="index" :key="index">
            <swiper-item>
                <image :src="item.url" class="slide-image" mode="aspectFill" style="width:100%;"/>
            </swiper-item>
        </block>
      </swiper>
    </div>
    <rmtitle :title="热门精选"></rmtitle>
    <div class="width_pro flex_around">
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
    </div>
    <!-- 排行榜 -->
    <phtitle></phtitle>
    <div class="width_pro" style="overflow-x:scroll;">
      <div class="overflow_pro">
        <div class="card_pro">
            <div class="card_top_pro" style="color:#A59167;">点击榜</div>
            <div style="height:553rpx;overflow-y:auto;">
              <paihangList v-for="item in 5" :key="item"></paihangList>
            </div>
        </div>
        <div class="card_pro">
            <div class="card_top_pro" style="color:#A59167;background:linear-gradient(90deg,rgba(233,238,249,1),rgba(253,252,248,0.99));">推荐榜</div>
            <div style="height:553rpx;overflow-y:auto;">
              <paihangList v-for="item in 5" :key="item"></paihangList>
            </div>
        </div>
        <div class="card_pro">
            <div class="card_top_pro" style="color:#A59167;">完结榜</div>
            <div style="height:553rpx;overflow-y:auto;">
              <paihangList v-for="item in 5" :key="item"></paihangList>
            </div>
        </div>
        <div class="card_pro">
            <div class="card_top_pro" style="color:#A59167;">热搜榜</div>
            <div style="height:553rpx;overflow-y:auto;">
              <paihangList v-for="item in 5" :key="item"></paihangList>
            </div>
        </div>
        <div class="card_pro">
            <div class="card_top_pro" style="color:#A59167;">收藏榜</div>
            <div style="height:553rpx;overflow-y:auto;">
              <paihangList v-for="item in 5" :key="item"></paihangList>
            </div>
        </div>
      </div>
     
    </div>
    <zxtitle :title="'经典完本'"></zxtitle>
    <bookListFour></bookListFour>
    <div class="width_pro flex_around">
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
      <div class="colnum_flex" @click="readClick">
        <img src="/static/icon/error.png" alt="">
        <span>王牌特工哈哈哈</span>
      </div>
    </div>
    <zxtitle :title="'最新专题'"></zxtitle>
    <div class="width_pro img_pro">
        <img src="/static/icon/error.png" alt="">
        <img src="/static/icon/error.png" alt="">
        <img src="/static/icon/error.png" alt="">
        <img src="/static/icon/error.png" alt="">
    </div>
    <zxtitle :title="'猜你喜欢'"></zxtitle>
    <div v-for="item in 3" :key="item" style="margin-bottom:40rpx;">
      <bookListFour></bookListFour>
    </div>
  </div>
</template>

<script>
import rmtitle from '@/components/rmtitle'
import phtitle from '@/components/phtitle'
import zxtitle from '@/components/zxtitle'
import bookListFour from '@/components/bookListFour'
import classify from '@/components/classify'
import paihangList from '@/components/paihangList'

export default {
  data(){
    return {
      active:1,
      movies:[
        {url:require("../../../static/icon/error.png")},
        {url:require("../../../static/icon/error.png")},
        {url:require("../../../static/icon/error.png")}
      ]
    }
  },
  components:{rmtitle,phtitle,zxtitle,classify,bookListFour,paihangList},
  onShow(){

    },
  mounted() {

  },
  methods:{
    readClick(){
      var url="../booksCover/main";
      mpvue.navigateTo({url})
    }
  }
  
}
</script>

<style scoped>
.width_pro{
  width:670rpx;
  margin:20rpx auto;
}
.flex_around{
  display: flex;
  justify-content: space-between;
}
.colnum_flex{
  width:144rpx;
  display:flex;
  flex-direction:column;
}
.colnum_flex>img{
  width:144rpx;
  height:198rpx;
  margin-bottom:10rpx;
}
.colnum_flex>span{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
.img_pro{
  display:flex;
  flex-wrap: wrap;
  justify-content:space-between;
  margin-bottom:0rpx;
}
.img_pro>img{
  width:320rpx;
  height: 150rpx;
  margin-bottom:32rpx;
}
.overflow_pro{
  width:2500rpx;
  display:flex;
}
.card_pro{
  width:460rpx;
  height:635rpx;
  margin-right:32rpx;
  box-shadow:0rpx 0rpx 68rpx 0rpx rgba(0, 0, 0, 0.1);
}
.card_top_pro{
  padding:0 40rpx;
  height:82rpx;
  line-height:82rpx;
  font-size:28rpx;
  font-weight:bold;
  background:linear-gradient(90deg,rgba(240,237,230,1),rgba(253,252,248,0.99));
}
/* 设置小程序单页面背景 */
page {
  background-color:white;
} 
</style>
