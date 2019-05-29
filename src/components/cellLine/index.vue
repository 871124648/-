<template>
  <div class="cellLine">
    <div class="flex_pro">
      <img :src="items.icons" alt="">
      <div class="book_list_content">
        <p style="font-size:26rpx;font-weight:600;color:#323237;">{{items.title}}</p>
        <span style="color:#D8D8D8;" v-if="items.pres">{{items.pres}}</span>
      </div>
      <div class="right_cell">
        <van-icon name="arrow" size="28rpx" color="#D8D8D8" style="margin-top:4rpx;"/>
        <span style="margin-right:20rpx;" v-if="items.rtxt" >{{items.rtxt}}</span>
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
    items:{

    }
  },
  methods:{

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.cellLine{
  background:white;
  padding:25rpx 40rpx;
  margin-top:20rpx;
}
.flex_pro{
  display: flex;
  align-items: center;
}
.ify-pro-right{
  width:140rpx;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.cellLine>.flex_pro img{
  width:44rpx;
  height:44rpx;
  margin-right:20rpx;
}
.book_list_content{
  width:420rpx;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
  display:flex;
  flex-direction:column;
  justify-content: space-around;
}
.flex{
  display: flex;
}
.right_cell{
  width:200rpx;
  display: flex;
  flex-direction: row-reverse;
}
</style>
