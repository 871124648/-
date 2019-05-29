<template>
  <div class="recharge" :class="isblack?'backgroundBlack':''">
      <div class="flex_between">
        <p>余额 <span style="color:#1ABC9C;">25</span> 金币</p>
        <span style="color:#95959A;">本章共计 &nbsp; 25 金币</span>
      </div>
      <button class="btn_pro">前往充值</button>
      <div class="flex_pro">
        <div class="flex">
          <img src="/static/icon/left.png" alt="" style="margin-right:4rpx;margin-top:4rpx;">
          <span>上一章</span>
        </div>
        <div class="flex">
          <img src="/static/icon/mulu.png" alt="" style="margin-right:4rpx;">
          <span>目录</span>
        </div>
        <div class="flex">
          <span>下一章</span>
          <img src="/static/icon/right.png" alt="" style="margin-left:4rpx;">
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
  props:{
    isblack:{
      type: Boolean,
      default:false
    }
  },
  mounted() {
    console.log(typeof this.isblack)
  },
  methods:{

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.recharge{
  width:750rpx;
  box-sizing:border-box;
  padding:30rpx 40rpx; 
  background:white;
}
.recharge img{
  width:24rpx;
  height:24rpx;
}
.flex_pro{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.flex{
  display:flex;
  align-items: center;
}
.flex_between{
    display:flex;
    justify-content: space-between;
    align-items: center;
}
.btn_pro{
  color:white;
  margin:30rpx 0;
  background:rgba(26,188,156,1);
  opacity:0.7;
  border-radius:4rpx;
}
.backgroundBlack{
  background:#262626;
}




</style>
