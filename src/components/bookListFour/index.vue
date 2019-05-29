<template>
  <div class="bookListFour">
    <div class="flex_pro">
      <div style="width:180rpx;">
        <img src="/static/icon/error.png" alt="">
      </div>
      <div class="book_list_content">
        <p class="p_title">一怒为红颜（直男专区）</p>
        <div style="margin:25rpx 0">
          <span>终结小猪猪 · 玄幻 &nbsp;&nbsp; 12884次点击</span>
        </div>
        <p class="p_content">天知道他刷了多久的副本才打下今日的江山吾 爱美人，更爱自己，谁人不知红颜媚，未来的..</p>
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
.bookListFour{
  background:white;
  padding:0rpx 40rpx;
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
.bookListFour>.flex_pro img{
  width:144rpx;
  height:198rpx;
}
.book_list_content{
  width:500rpx;
  /* overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap; */
}
.flex{
  display: flex;
}
.flex-column{
  display: flex;
  flex-direction:column;
  justify-content:center;
}
.p_content{
   color:#323237;
   overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}
</style>
