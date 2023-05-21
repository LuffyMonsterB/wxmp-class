<template>
  <view>
    <view class="flex justify-center">
      <view
        class="cu-avatar xl round"
        style="
          background-image: url(https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fpic1.zhimg.com%2Fv2-83cc8e249feb265d536ec3ae2e55f8bb_1440w.jpg%3Fsource%3D172ae18b&refer=http%3A%2F%2Fpic1.zhimg.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1650977398&t=ef3349e3fa06fbea216677f807eebe7c);
        "
      ></view>
    </view>
    <view class="flex justify-center">
      <view class="text-xl">{{ userInfo.nickName }}</view>
    </view>
    <!-- 会员 -->
    <view class="flex justify-center margin-lr margin-top">
      <navigator
        open-type="navigate"
        hover-class="animation-fade"
        url="/pages/Vip/Vip"
        class="nav-li bg-cyan"
      >
        <view class="nav-title">我的会员</view>
        <view class="nav-name">VIP</view>
        <text class="cuIcon-favor"></text>
      </navigator>
    </view>
    <view class="flex justify-center margin-lr">
      <OrderCard style="width:100%"/>
    </view>
    <view class="flex justify-center margin-lr">
      <UserInfoList style="width:100%"/>
    </view>
  </view>
</template>

<script>
import OrderCard from 'components/OrderCard/OrderCard'
import UserInfoList from 'components/UserInfoList/UserInfoList'
export default {
  components:{OrderCard,UserInfoList},
  data() {
    return {
      userInfo: {
        nickName: "路飞大魔王",
        phone: "12345678",
      },
      navigatorList: [
        { name: "checker", title: "审核员", color: "purple", icon: "profile" },
        { name: "annotator", title: "标注员", color: "cyan", icon: "write" },
      ],
    };
  },
};
</script>

<style scoped>
page {
  height: 100%;
}
.my-background {
  width: 100%;
  height: 100%;
  position: fixed;
  background-size: 100% 100%;
  z-index: -1;
}
</style>
