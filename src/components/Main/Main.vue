<template>
  <view>
    <!-- swiper -->
    <swiper
      class="screen-swiper square-dot"
      indicator-dots="true"
      circular="true"
      autoplay="true"
      interval="4000"
      duration="500"
      indicator-active-color="#1cbbb4"
    >
      <swiper-item v-for="(item, index) in swiperList" :key="index">
        <image
          :src="item.url"
          mode="aspectFill"
          class="swiper-content"
          v-if="item.type == 'image'"
        ></image>
        <video
          :src="item.url"
          autoplay
          loop
          muted
          class="swiper-content"
          :show-play-btn="false"
          :controls="false"
          objectFit="cover"
          v-if="item.type == 'video'"
        ></video>
      </swiper-item>
    </swiper>
    <Classification />
    <!-- video -->
    <view class="flex justify-center padding" style="width: 100%">
      <video
        object-fit="fill"
        :poster="posterUrl"
        :src="videoUrl"
        binderror="videoErrorCallback"
        class="video"
      ></video>
    </view>
    <!-- 近期课程 -->
    <view class="flex justify-center">
      <view
        class="bg-cyan shadow margin-sm padding-xs"
        style="width: 100%; border-radius: 10rpx"
        >近期课程</view
      >
    </view>
    <view>
    <ClassCard  v-for="item in classList" :key="item.id" :classInfo="item"/>
    </view>
    
  </view>
</template>

<script>
import Classification from "components/Classification/Classification";
import ClassCard from "components/ClassCard/ClassCard";
export default {
  components: { Classification, ClassCard },
  data() {
    return {
      swiperList: [
        {
          id: 0,
          type: "image",
          url: "/static/swiper/banner.jpg",
        },
        {
          id: 1,
          type: "image",
          url: "/static/swiper/banner.jpg",
        },
        {
          id: 2,
          type: "image",
          url: "/static/swiper/banner.jpg",
        },
        {
          id: 3,
          type: "image",
          url: "/static/swiper/banner.jpg",
        },
        {
          id: 4,
          type: "image",
          url: "/static/swiper/banner.jpg",
        },
        {
          id: 5,
          type: "image",
          url: "/static/swiper/banner.jpg",
        },
        {
          id: 6,
          type: "image",
          url: "/static/swiper/banner.jpg",
        },
      ],
      classList:[
        {id:'1',imgUrl:"https://img0.baidu.com/it/u=2959864821,4281850450&fm=253&fmt=auto&app=120&f=JPEG?w=1154&h=800",tag:'热卖',description:'课程描述xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx',title:'3.26/3.27英式低阶海盗寻宝记',time:'3.26/3.27',location:'西溪幼儿园',member:'4-6人',price:'888'},
        {id:'2',imgUrl:"https://img0.baidu.com/it/u=2959864821,4281850450&fm=253&fmt=auto&app=120&f=JPEG?w=1154&h=800",tag:'热卖',description:'课程描述xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx',title:'3.26/3.27英式低阶海盗寻宝记',time:'3.26/3.27',location:'西溪幼儿园',member:'4-6人',price:'888'},
        {id:'3',imgUrl:"https://img0.baidu.com/it/u=2959864821,4281850450&fm=253&fmt=auto&app=120&f=JPEG?w=1154&h=800",tag:'热卖',description:'课程描述xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx',title:'3.26/3.27英式低阶海盗寻宝记',time:'3.26/3.27',location:'西溪幼儿园',member:'4-6人',price:'888'},
        {id:'4',imgUrl:"https://img0.baidu.com/it/u=2959864821,4281850450&fm=253&fmt=auto&app=120&f=JPEG?w=1154&h=800",tag:'热卖',description:'课程描述xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx',title:'3.26/3.27英式低阶海盗寻宝记',time:'3.26/3.27',location:'西溪幼儿园',member:'4-6人',price:'888'},
      ],
      posterUrl:
        "https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fmgr.91sst.com%2FContent%2Fjs%2Fueditor%2Fnet%2Fupload%2Fimage%2F20181021%2F6367572202006768238389199.jpg&refer=http%3A%2F%2Fmgr.91sst.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1650802736&t=cd22579a5e071d2a5a22e167e990aba6",
      videoUrl:
        "http://wxsnsdy.tc.qq.com/105/20210/snsdyvideodownload?filekey=30280201010421301f0201690402534804102ca905ce620b1241b726bc41dcff44e00204012882540400&bizid=1023&hy=SH&fileparam=302c020101042530230204136ffd93020457e3c4ff02024ef202031e8d7f02030f42400204045a320a0201000400",
    };
  },
};
</script>

<style scoped>
.video {
  width: 100%;
  border: 10rpx solid #1cbbb4;
  border-radius: 20rpx;
}
</style>
