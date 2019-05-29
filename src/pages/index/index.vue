<template>
  <div class="my_pro">
    <div class="topCard">
        <div class="flex_pro">
          <img src="/static/icon/error.png" alt="">
          <div class="txt_pro">
            <p style="margin-bottom:28rpx;">白色黑裤衩，你好</p>
            <span>账户资产 2200 金币</span>
          </div>
          <div class="readBtn flex">
            <img src="/static/icon/user-qd.png" alt="">
            <span style="margin-top:4rpx;">签到</span>
          </div>
        </div>
    </div>

    <div v-for="item in cellList" :key="item">
      <cellLine :items="item"></cellLine>
    </div>
  </div>
</template>

<script>
import cellLine from '@/components/cellLine'
export default {
  data () {
    return {
      active:3,
      cellList:[
        {icons:"/static/icon/user-zh.png",title:"我的账户",pres:"",rtxt:"前往充值"},
        {icons:"/static/icon/user-vip.png",title:"超级VIP",pres:"开通会员，免广告畅读",rtxt:"立即开通"},
        {icons:"/static/icon/user-yq.png",title:"我的邀请",pres:"",rtxt:""},
        {icons:"/static/icon/user-sd.png",title:"我的书单",pres:"",rtxt:""},
        {icons:"/static/icon/user-rl.png",title:"我的签到",pres:"",rtxt:""},
        {icons:"/static/icon/user-ly.png",title:"留言反馈",pres:"",rtxt:""},
      ]
    }
  },
  components:{cellLine},
  onShow(){
    },
  methods: {
    // bindViewTap () {
    //   const url = '../logs/main'
    //   if (mpvuePlatform === 'wx') {
    //     mpvue.switchTab({ url })
    //   } else {
    //     // mpvue.navigateTo({ url })
    //   }
    // },
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
@import "../../app.wxss";
.my_pro{
  color:#323237;
}
.topCard{
  width:670rpx;
  box-sizing:border-box;
  background:white;
  padding:40rpx 30rpx;
  margin:40rpx auto;
  box-shadow:0rpx 0rpx 68rpx 0rpx rgba(0, 0, 0, 0.1);
}
.flex_pro{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.topCard>.flex_pro>img{
  width:80rpx;
  height:80rpx;
  border-radius: 50%;
}
.flex{
  display:flex;
  align-items: center;
  justify-content: center;
}

.readBtn{
  font-size:24rpx;
  width:160rpx;
  height:63rpx;
  line-height:63rpx;
  border-radius: 50rpx;
  color:white;
  background:linear-gradient(90deg,rgba(29,188,156,1),rgba(59,225,192,1));
}
.txt_pro{
  width:300rpx;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space: nowrap;
}
.txt_pro p{
  font-size:32rpx;
  font-weight:bold;
}
.readBtn>img{
  width:32rpx;
  height:32rpx;
  margin-right:10rpx;
}
.cell_pro{
  width:730rpx;
  margin:0 auto;
}


</style>
