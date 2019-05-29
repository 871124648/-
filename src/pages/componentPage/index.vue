<template>
  <div class="componentPage">
    <tabbarBottom></tabbarBottom>
    <classify></classify>
    <classifyline></classifyline>
    <sltitle></sltitle>
    <zxtitle></zxtitle>
    <rmtitle></rmtitle>
    <phtitle></phtitle>
    <bookListOne></bookListOne>
    <bookListTwo></bookListTwo>
    <bookListThree></bookListThree>
    <lineCard></lineCard>
    <DetailCard></DetailCard>
    <beginRead></beginRead>
    <bookListFour></bookListFour>
    <DetailCardRate></DetailCardRate>
    <sectionpage></sectionpage>
    <editComponent></editComponent>
    <editBlackComponent></editBlackComponent>
  </div>
</template>

<script>
import tabbarBottom from '@/components/tabbarBottom'
import classify from '@/components/classify'
import classifyline from '@/components/classifyline'
import sltitle from '@/components/sltitle'
import zxtitle from '@/components/zxtitle'
import rmtitle from '@/components/rmtitle'
import phtitle from '@/components/phtitle'
import bookListOne from '@/components/bookListOne'
import bookListTwo from '@/components/bookListTwo'
import bookListThree from '@/components/bookListThree'
import lineCard from '@/components/lineCard'
import DetailCard from '@/components/DetailCard'
import beginRead from '@/components/beginRead'
import bookListFour from '@/components/bookListFour'
import DetailCardRate from '@/components/DetailCardRate'
import sectionpage from '@/components/sectionpage'
import editComponent from '@/components/editComponent'
import editBlackComponent from '@/components/editBlackComponent'
export default {
  data(){
    return {
    }
  },
  components:{tabbarBottom,classify,classifyline,sltitle,zxtitle,rmtitle,phtitle,bookListOne,bookListTwo,bookListThree,lineCard,DetailCard,beginRead,bookListFour,DetailCardRate,sectionpage,editComponent,editBlackComponent},
  mounted() {

  },
  methods:{
  }
  
}
</script>

<style>
.componentPage{
  background:#F2F2F7;
  height:100%;
}
/* 设置小程序单页面背景 */
page {
  background-color: #F2F2F7;
} 
</style>
