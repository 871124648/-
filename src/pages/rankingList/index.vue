<template>
  <div class="rankingList">
      <div class="left_pro">
        <div v-for="(item,index) in titleData" :key="index" class="cell_pro" :class="index==dex?'active':''" @click="dexClick(index)">{{item}}</div>
      </div>
      <div class="right_pro">
        <div v-for="item in 9" :key="item">
          <bookListOne></bookListOne>
        </div>
      </div>
  </div>
</template>

<script>
import bookListOne from '@/components/bookListOne'
export default {
    data(){
    return {
      titleData:["点击榜","推荐榜","完结榜","热搜榜","收藏榜"],
      dex:0
    }
  },
  components:{bookListOne},
  onShow(){

    },
  mounted() {

  },
  methods:{
    dexClick(index){
      this.dex = index;
    }
  }
}
</script>

<style scoped>
.rankingList{
  display: flex;
}
.left_pro{
  width:160rpx;
  height:1206rpx;
  overflow-y: auto;
  background:rgba(245,245,247,1);
}
.right_pro{
  height:1206rpx;
  overflow-y: auto;
}
.cell_pro{
  height:100rpx;
  line-height:100rpx;
  color:#96969B;
  text-align:center;
  font-size:28rpx;
}
.active{
  color:#222222;
  background:white;
}

</style>
