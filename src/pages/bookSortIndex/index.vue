<template>
  <div class="bookSortIndex">
    <div v-for="item in sortData" :key="item" class="car_sort_pro">
      <bookSort :items="item"></bookSort>
    </div>
  </div>
</template>

<script>
import bookSort from '@/components/bookSort'
export default {
    data(){
    return {
      active:2,
      sortData:[
        {imgUrl:"/static/icon/error.png",title:"悬疑灵异",num:"2918"},
        {imgUrl:"/static/icon/error.png",title:"仙侠科幻",num:"2918"},
        {imgUrl:"/static/icon/error.png",title:"悬疑灵异",num:"2918"},
        {imgUrl:"/static/icon/error.png",title:"仙侠科幻",num:"2918"},
        {imgUrl:"/static/icon/error.png",title:"悬疑灵异",num:"2918"},
        {imgUrl:"/static/icon/error.png",title:"仙侠科幻",num:"2918"},
        {imgUrl:"/static/icon/error.png",title:"悬疑灵异",num:"2918"},
      ]
    }
  },
  components:{bookSort},
  onShow(){

    },
  mounted() {

  },
  methods:{

  }
}
</script>

<style scoped>
.bookSortIndex{
  padding:40rpx;
  display:flex;
  flex-wrap:wrap;
  justify-content: space-between;
}
.car_sort_pro{
  margin-bottom:30rpx;
  width:320rpx;
  height:170rpx;
  box-shadow:0rpx 0rpx 68rpx 0rpx rgba(0, 0, 0, 0.1);
}
</style>
