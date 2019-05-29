<template>
  <div class="bookRack">
    <van-search v-model="searchValue" shape="round" placeholder="大铁棍子医院，找铜主任"  @focus="inputFocus" use-action-slot>
      <div slot="action" style="background:#F7F8FA;color:#747479;position:relative;left:-20rpx;top:0;padding:0 30rpx;border-radius:0rpx 30rpx 30rpx 0;">
        <div style="width:30rpx;background:#F7F8FA;position:absolute;left:-28rpx;top:0;">&nbsp;</div>
        <span style="padding-left:30rpx;border-left:1px solid #E3E3E6;">阅读记录</span>
      </div>
    </van-search>
    <lineCard></lineCard>
    <div v-for="item in 10" :key="item">
      <bookListTwo></bookListTwo>
    </div>
    <div style="padding:25rpx 40rpx;">
      <div class="flex_pro">
        <div style="width:160rpx;">
          <img src="/static/icon/addImg.png" alt="">
        </div>
        <div></div>
        <div></div>
      </div>
    </div>
  </div>
</template>

<script>
import bookListTwo from '@/components/bookListTwo'
import lineCard from '@/components/lineCard'
export default {
  data(){
    return {
      active:0,
      searchValue:""
    }
  },
  components:{bookListTwo,lineCard},
    onShow(){

    },
  mounted() {
  },
  methods:{
      inputFocus(){
        var url = '../searchIndex/main'
        mpvue.navigateTo({ url })
      },
  }
  
}
</script>

<style scoped>
.flex_pro{
  display: flex;
}
.bookRack .flex_pro img{
  width:120rpx;
  height:160rpx;
}
/* 设置小程序单页面背景 */
page {
  background-color: white;
} 
</style>
