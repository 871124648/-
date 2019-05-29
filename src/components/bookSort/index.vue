<template>
  <div class="paihangList">
    <div class="flex_pro">
      <div style="margin-right:20rpx;">
        <img :src="items.imgUrl" alt="">
      </div>
      <div class="book_list_content">
        <p class="p_title" style="margin:6rpx 0;">{{items.title}}</p>
        <span>共{{items.num}}本</span>
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
  width:80rpx;
  height:110rpx;
}
.book_list_content{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
</style>
