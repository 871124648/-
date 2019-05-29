<template>
  <div class="bookList">
    <div v-for="(item,index) in dataList" :key="index">
      <DetailCard :items="item" :dex="index" @iszanClick="iszanClick" @iscollectClick="iscollectClick"></DetailCard>
    </div>
  </div>
</template>

<script>
import DetailCard from '@/components/DetailCard'
export default {
    data(){
    return {
      active:2,
      dataList:[
        {iszan:false,iscollect:false,title:"一怒为红颜（直男专区）",name:"终结小猪猪",types:"宠文",s1:"我吃西红柿",s2:"连载·玄幻·182万字",s3:"天知道他刷了多久的副本才打下今日的江山，吾爱美人更爱自己，谁人不知红颜媚，一剑挑的珠帘翠。"},
        {iszan:false,iscollect:false,title:"一怒为红颜（直男专区）",name:"终结小猪猪",types:"宠文",s1:"我吃西红柿",s2:"连载·玄幻·182万字",s3:"天知道他刷了多久的副本才打下今日的江山，吾爱美人更爱自己，谁人不知红颜媚，一剑挑的珠帘翠。"},
        {iszan:false,iscollect:false,title:"一怒为红颜（直男专区）",name:"终结小猪猪",types:"宠文",s1:"我吃西红柿",s2:"连载·玄幻·182万字",s3:"天知道他刷了多久的副本才打下今日的江山，吾爱美人更爱自己，谁人不知红颜媚，一剑挑的珠帘翠。"},
      ]
    }
  },
  components:{DetailCard},
  onShow(){

    },
  mounted() {

  },
  methods:{
    iszanClick(data){
      this.dataList[data.dex].iszan = !data.val;
    },
    iscollectClick(data){
       this.dataList[data.dex].iscollect = !data.val;
    }
  }
}
</script>

<style>

</style>
