<template>
  <div>
      <x-header :right-options="{showMore: true}" :left-options="{showBack: false}">wle</x-header>
      <swiper loop auto :list="demo06_list" :index="demo06_index" ></swiper>
    <tabbar>
      <tabbar-item selected link="http://www.nvliu.me" >
        <img slot="icon" src="../assets/首页.png">
        <span slot="label">首页</span>
      </tabbar-item>
      <tabbar-item show-dot selected link="https://www.douyu.com/156277">
        <img slot="icon" src="../assets/直播.png">
        <span slot="label">直播间</span>
      </tabbar-item>
      <tabbar-item selected>
        <img slot="icon" src="../assets/录像.png" >
        <span slot="label">录像</span>
      </tabbar-item>
      <tabbar-item   >
        <img slot="icon" src="../assets/关注.png">
        <span slot="label">登陆</span>
      </tabbar-item>
    </tabbar>
    <panel :header="推荐" :footer="footer" :list="list" :type="type"></panel>
  </div>
</template>

<script>
import { Tabbar, TabbarItem, Group, Cell, XHeader, Swiper, Panel } from 'vux'
const baseList = [{
  url: 'javascript:',
  img: 'https://ww1.sinaimg.cn/large/663d3650gy1fq66vvsr72j20p00gogo2.jpg',
  title: '送你一朵fua'
}, {
  url: 'javascript:',
  img: 'https://ww1.sinaimg.cn/large/663d3650gy1fq66vw1k2wj20p00goq7n.jpg',
  title: '送你一辆车'
}, {
  url: 'javascript:',
  img: 'https://static.vux.li/demo/5.jpg', // 404
  title: '送你一次旅行',
  fallbackImg: 'https://ww1.sinaimg.cn/large/663d3650gy1fq66vw50iwj20ff0aaaci.jpg'
}]
const urlList = baseList.map((item, index) => ({
  url: 'http://m.baidu.com',
  img: item.img,
  fallbackImg: item.fallbackImg,
  title: `(可点击)${item.title}`
}))

export default {
  components: {
    Swiper,
    XHeader,
    Tabbar,
    TabbarItem,
    Group,
    Cell,
    Panel
  },
  data () {
    return {
      demo06_list: urlList,
      demo06_index: 0
    }
  }

}
</script>