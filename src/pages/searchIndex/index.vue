<template>
  <div class="searchIndex">
      <van-search v-model="value" shape="round" placeholder="大铁棍子医院，找铜主任" />
      <rmtitle :title="'猜你喜欢'"></rmtitle>
      <div v-for="item in 3" :key="item">
        <bookListThree></bookListThree>
      </div>
      <sltitle></sltitle>
      <div class="width_pro flex_wrap">
        <van-button type="default" v-for="item in dataLsit" :key="item" size="small" style="margin:0rpx 20rpx 20rpx 0rpx;">{{item}}</van-button>
      </div>
      <div v-for="item in 5" :key="item" style="margin-bottom:40rpx;">
        <bookListFour></bookListFour>
      </div>

  </div>
</template>

<script>
import rmtitle from '@/components/rmtitle'
import sltitle from '@/components/sltitle'
import bookListThree from '@/components/bookListThree'
import bookListFour from '@/components/bookListFour'
export default {
    data(){
    return {
        dataLsit:["天上人间","王婆卖瓜自卖","征途","我与隔壁老王的女儿"]
    }
  },
  components:{rmtitle,sltitle,bookListThree,bookListFour},
  mounted() {

  },
  methods:{

  }
}
</script>

<style>
.flex_wrap{
  display:flex;
  flex-wrap:wrap;
}
</style>
