<template>
  <div class="bookListThree">
    <div class="flex_pro">
      <div style="width:100rpx;">
        <img src="/static/icon/error.png" alt="">
      </div>
      <div class="book_list_content">
        <p class="p_title" style="margin:10rpx 0;">怒江</p>
        <div class="flex"><b style="font-size:26rpx;color:#323237;margin-right:40rpx;">我吃西红柿</b><span> 连载·玄幻·182万字</span></div>
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

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.bookListThree{
  background:white;
  padding:15rpx 40rpx;
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
.bookListThree>.flex_pro img{
  width:80rpx;
  height:110rpx;
}
.book_list_content{
  width:500rpx;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
.flex{
  display:flex;
}
</style>
