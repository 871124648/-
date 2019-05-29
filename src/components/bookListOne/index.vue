<template>
  <div class="bookListOne" @click="openDetail">
    <div class="flex_pro">
      <div style="width:160rpx;">
        <img src="/static/icon/error.png" alt="">
      </div>
      <div class="book_list_content">
        <p class="p_title" style="margin:20rpx 0;">鸡鸭鱼肉样样都有</p>
        <span>白色黑裤衩 · 20本 · 9193收藏</span>
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
    // 如果有其他页面引用这个组件，要先进行判断
    openDetail(){
      var url ="../bookListDetail/main"
      mpvue.navigateTo({url})
    }

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.bookListOne{
  background:white;
  padding:25rpx 40rpx;
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
.bookListOne>.flex_pro img{
  width:120rpx;
  height:160rpx;
}
.book_list_content{
  /* width:500rpx; */
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
</style>
