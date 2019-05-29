<template>
  <div class="paihangList">
    <div class="flex_pro">
      <div style="margin-right:30rpx;">
        <img src="/static/icon/error.png" alt="">
      </div>
      <div class="book_list_content">
        <p class="p_title" style="margin:20rpx 0;">算私命</p>
        <span>我吃西红柿</span>
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
.paihangList{
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
.paihangList>.flex_pro img{
  width:100rpx;
  height:138rpx;
}
.book_list_content{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
</style>
