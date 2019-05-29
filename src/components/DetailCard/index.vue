<template>
  <div class="DetailCard">
    <div class="flex_pro_column">
      <div class="flex_pro">
        <div style="width:170rpx;">
          <img src="/static/icon/error.png" alt="">
        </div>
        <div class="flex_pro_column" style="padding-bottom:40rpx;">
          <p class="p_title">{{items.title}}</p>
          <span style="font-size:28rpx;">{{items.name}}&nbsp;&nbsp;{{items.types}}</span>
          <div class="flex"><b style="font-size:26rpx;color:#323237;margin-right:40rpx;">{{items.s1}}</b><span> {{items.s2}}</span></div>
        </div>
      </div>
      <div style="margin:40rpx 0;">
        <p>{{items.s3}}</p>
      </div>
      <div class="bottom_pro">
        <div style="width:400rpx;">
          <img v-if="items.iszan" src="/static/icon/zan-on.png" alt="" @click="iszanClick">
          <img v-if="!items.iszan" src="/static/icon/zan.png" alt="" @click="iszanClick">
          <img v-if="items.iscollect" src="/static/icon/shoucang-on.png" alt="" @click="iscollectClick">
          <img v-if="!items.iscollect" src="/static/icon/shoucang.png" alt="" @click="iscollectClick">
        </div>
        <div>
          <button class="readBtn" @click="btnClick">查看书单</button>
        </div>
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
  props:{
    items:{},
    dex:{}
  },
  methods:{
    btnClick(){
      var url = '../bookListIndex/main'
      mpvue.navigateTo({ url })
    },
    iszanClick(){
      this.$emit("iszanClick",{dex:this.dex,val:this.items.iszan})
    },
    iscollectClick(){
      this.$emit("iscollectClick",{dex:this.dex,val:this.items.iscollect})
    }
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.DetailCard{
  width:670rpx;
  box-sizing:border-box;
  background:white;
  padding:40rpx 30rpx;
  margin:40rpx auto;
  box-shadow:0rpx 0rpx 68rpx 0rpx rgba(0, 0, 0, 0.1);
}
.flex_pro{
  display: flex;
}
.flex_pro_column{
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
.DetailCard .flex_pro img{
  width:144rpx;
  height:198rpx;
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
.bottom_pro{
  display: flex;
  justify-content:space-around;
  align-items:center;
}
.bottom_pro img{
  width:42rpx;
  height:42rpx;
  margin-right:72rpx;
}



</style>
