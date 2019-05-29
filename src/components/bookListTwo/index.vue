<template>
  <div class="bookListTwo">
    <div class="flex_pro" @click="openBook">
      <div style="width:160rpx;">
        <img src="/static/icon/error.png" alt="">
      </div>
      <div class="book_list_content">
        <p class="p_title">怒江</p>
        <div class="flex"><b style="font-size:26rpx;color:#323237;">我吃西红柿</b><span> · 218章未读</span></div>
        <span>在读 第四百一十章  狂雨来袭</span>
      </div>
      <div class="flex-column">
        <!-- <img src="/static/icon/caozuo.png" alt="" style="width:60rpx;height:60rpx;"> -->
        <van-icon name="ellipsis" size="18px" style="margin-top:5px;"/>
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
  methods:{
    openBook(){
      var url="../booksCover/main";
      mpvue.navigateTo({url});
    }
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.bookListTwo{
  background:white;
  padding:25rpx 40rpx;
  margin-top:20rpx;
}
.flex_pro{
  display: flex;
}
.ify-pro-right{
  width:140rpx;
  display: flex;
  justify-content:space-between;
  align-items:center;
}
.title_pro{
  color:#333333;
  font-size:34rpx;
  font-weight:900;
}
.bookListTwo>.flex_pro img{
  width:120rpx;
  height:160rpx;
}
.book_list_content{
  width:450rpx;
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
.flex-column{
  display: flex;
  flex-direction:column;
  justify-content:center;
}
</style>
