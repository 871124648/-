<template>
  <div class="tabbarBottom">
    <!-- 目前不为苹果底部预留距离 -->
    <van-tabbar :active="active" active-color="#28C0A2" @change="tabChange" :safe-area-inset-bottom="false">
      <van-tabbar-item>
        <image
          slot="icon"
          src="/static/tabs/sj.png"
          mode="aspectFit"
        />
        <image
          slot="icon-active"
          src="/static/tabs/sjd.png"
          mode="aspectFit"
        />
        书架
      </van-tabbar-item>
      <van-tabbar-item>
        <image
          slot="icon"
          src="/static/tabs/sc.png"
          mode="aspectFit"
        />
        <image
          slot="icon-active"
          src="/static/tabs/scd.png"
          mode="aspectFit"
        />
        书城
      </van-tabbar-item>
      <van-tabbar-item>
        <image
          slot="icon"
          src="/static/tabs/sd.png"
          mode="aspectFit"
        />
        <image
          slot="icon-active"
          src="/static/tabs/sdd.png"
          mode="aspectFit"
        />
        书单
      </van-tabbar-item>
      <van-tabbar-item>
        <image
          slot="icon"
          src="/static/tabs/my.png"
          mode="aspectFit"
        />
        <image
          slot="icon-active"
          src="/static/tabs/myd.png"
          mode="aspectFit"
        />
        我的
      </van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
export default {
   data(){
    return {
    }
  },
  props:{
    active:{
      default:0
    }
  },
  mounted() {
  },
  onLoad(){
    console.log("重新加载了")
  },
  // onShow(){
  //   console.log("每次必须触发")
  //   var pages = getCurrentPages() //获取加载的页面
  //   var currentPage = pages[pages.length - 1] //获取当前页面的对象
  //   var url = currentPage.route //当前页面url
  //     var start = url.indexOf('/');
  //     var end = url.lastIndexOf('/');
  //     url = url.substring(start,end);
  //     console.log(url);
  //     if(url=="/bookRack"){
  //       console.log("进来改变",this.active)
  //       this.active = 0;
  //     }else if(url=="/bookCity"){
  //       this.active = 1;
  //     }else if(url=="/bookList"){
  //       this.active = 2;
  //     }else if(url=="/index"){
  //       this.active = 3;
  //     }
  //   },

  methods:{
    // 获取返回地N次出现的字符
    find(str, cha, num) {
        var x = str.indexOf(cha);
        for (var i = 0; i < num; i++) {
            x = str.indexOf(cha, x + 1);
        }
        return x;
    },
    tabChange(e){
      var urlArr = ['../bookRack/main','../bookCity/main','../bookList/main','../index/main',]
      var url = urlArr[e.mp.detail];
      console.log(url)
      mpvue.navigateTo({ url })
    }
  }
}
</script>

<style>
.card {
  padding: 10px;
}
</style>
