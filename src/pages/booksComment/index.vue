<template>
  <div class="booksComment">
    <div class="rate_pro">
      <van-rate :value="rateValue" size="24"/>
    </div>
    <div class="bottom_pro">
      <textarea rows="10" placeholder="点评这本书..." maxlength="200"></textarea>
    </div>
  </div>
</template>

<script>
import DetailCard from '@/components/DetailCard'
export default {
    data(){
    return {
      rateValue:0
    }
  },
  components:{DetailCard},
  onShow(){

    },
  mounted() {

  },
  methods:{

  }
}
</script>

<style scoped>
.rate_pro{
  text-align:center;
}
.bottom_pro{
  padding:40rpx;
}
.bottom_pro textarea{
  width:100%;
  font-size:28rpx;
}
</style>
