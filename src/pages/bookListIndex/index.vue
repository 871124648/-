<template>
  <div class="bookListIndex">
      <classifyline></classifyline>
      <div v-for="item in 10" :key="item">
        <bookListOne></bookListOne>
      </div>
  </div>
</template>

<script>
import classifyline from '@/components/classifyline'
import bookListOne from '@/components/bookListOne'

export default {
    data(){
    return {
        dataLsit:["天上人间","王婆卖瓜自卖","征途","我与隔壁老王的女儿"]
    }
  },
  components:{classifyline,bookListOne},
  mounted() {

  },
  methods:{

  }
}
</script>

<style>

</style>
