<template>
  <div class="lineCard">
    <div class="flex_pro">
      <!-- <img src="/static/icon/qiangtui.png" alt=""> -->
      <div style="width:400rpx" class="flex">
        <div class="old_span">
          强推
          <div></div>
        </div>
        <p class="book_list_content p_title">番茄新书《武逆苍穹》</p>
      </div>
      <div>
        <button class="readBtn">立即阅读</button>
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
.lineCard{
  width:670rpx;
  box-sizing:border-box;
  background:white;
  padding:40rpx 30rpx;
  margin:20rpx auto;
  box-shadow:0rpx 0rpx 68rpx 0rpx rgba(0, 0, 0, 0.1);
}
.flex_pro{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.lineCard img{
  width:60rpx;
  height:30rpx;
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
.old_span{
  font-weight:900;
  font-size:34rpx;
  color:#323237;
  margin-right:30rpx;
  position:relative;
}
.old_span>div{
  border:8rpx solid #FF414C;
  border-radius:50%;
  position:absolute;
  top:0;
  right:-10rpx;
}
.readBtn{
  padding:0 !important;
  font-size:24rpx;
  width:160rpx;
  height:50rpx;
  line-height:50rpx;
  border:none;
  outline: none;
  border-radius: 50rpx;
  color:white;
  background-color: #00E2BB;
  background:linear-gradient(90deg,rgba(29,188,156,1),rgba(59,225,192,1));
}


</style>
