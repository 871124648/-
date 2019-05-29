<template>
  <div class="sectionpage">
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
    }
  },
  methods:{

  }
}
</script>

<style scoped>
@import "../../app.wxss";
.sectionpage{
  width:670rpx;
  box-sizing:border-box;
  background:white;
  padding:30rpx 60rpx;
  margin:0rpx auto;
  margin-bottom:40rpx;
  color:#323237;
}
.flex_pro{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.sectionpage img{
  width:24rpx;
  height:24rpx;
}
.book_list_content{
  width:300rpx;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
.flex{
  display:flex;
  align-items: center;
}



</style>
