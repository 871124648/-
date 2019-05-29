<template>
  <div class="editComponent" ref="editComponent">
    <div class="flex_pro">
      <div>
        <p class="p_title">第一百章 &nbsp;&nbsp; 来自王的蔑视</p>
      </div>
      <div class="flex top_icon">
        <img src="/static/icon/left_black.png" alt="">
        <div class="slider_pro">
          <van-slider active-color="#323237"></van-slider>
        </div>
        <img src="/static/icon/right_black.png" alt="">
      </div>
      <div class="flex_between" v-if="takeShow">
        <span>自动订阅</span>
        <van-switch :checked="checked" size="20px" active-color="#00C099" @change="swithChange"/>
      </div>
      <div class="bottom_icon">
        <img src="/static/icon/mulu_black.png" alt="" @click="popupClick">
        <img src="/static/icon/shezhi_black.png" alt="" @click="rechargeClick">
        <img src="/static/icon/baitian.png" alt="" @click="tabClick">
        <img src="/static/icon/fangui_black.png" alt="" @click="edits">
      </div>

    </div>
  </div>
</template>

<script>
export default {
   data(){
    return {
      takeShow:false,
      checked:false
    }
  },
  methods:{
      edits(){
        this.takeShow = true;
      },
      swithChange(){
        this.checked = !this.checked;
        console.log(this.checked);
      },
      tabClick(){
         wx.setNavigationBarColor({
            frontColor: "#ffffff",/*标题颜色，这里貌似仅支持 #ffffff 和 #000000 */
            backgroundColor: "#262626",/*背景色 十六进制即可*/
            animation: {/*动画*/
              duration: 400,
              timingFunc: 'easeIn'
            }
        })
        // wx.createSelectorQuery().selectAll('.editComponent').boundingClientRect(function (rect) {
        //     console.log(rect[0].width)
        // }).exec()  
        this.$emit("tabClick",true)
      },
      popupClick(){
        this.$emit("popupClick")
      },
      rechargeClick(){
        this.$emit("rechargeClick")
      }
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.editComponent{
  background:white;
  padding:30rpx 60rpx;
  margin:0rpx auto;
  color:#323237;
}
.flex_pro{
  display: flex;
  flex-direction:column;
  justify-content: space-between;
  align-items: center;
}
.top_icon{
  margin-top:50rpx;
  margin-bottom:60rpx;
}
.top_icon img{
  width:24rpx;
  height:24rpx;
}
.bottom_icon{
  width:554rpx;
  margin:0 auto;
  display:flex;
  justify-content:space-between;
  align-items: center;  
}
.bottom_icon img{
  width:36rpx;
  height:36rpx;
}

.flex{
  display:flex;
  align-items: center;
}
.flex_between{
  width: 100%;
  margin-bottom:30rpx;
  display:flex;
  align-items: center;
  justify-content: space-between;
}
.slider_pro{
  width:554rpx;
  margin:0 30rpx;
}




</style>
