<template>
  <view class="cu-card bg-white shadow" style="border-radius: 12rpx">
    <view class="flex justify-between align-end padding-sm solid-bottom bg-cyan light">
      <view class="text-bold">我的课程</view>
      <view class="text-sm">全部></view>
    </view>
    <view>
      <view
        class="cu-list grid col-4 no-border"
        
      >
        <view class="cu-item" v-for="(item, index) in classList" :key="index">
          <view :class="['cuIcon-' + item.icon, 'text-' + item.color]">
            <view class="cu-tag badge" v-if="item.unread != 0">{{
              item.unread
            }}</view>
          </view>
          <text class="text-black">{{ item.name }}</text>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: "OrderCard",
  data() {
    return {
      classList: [
        {
          icon: "pay",
          color: "black",
          name: "待付款",
          unread: 0,
          path:'unpay'
        },
        {
          icon: "ticket",
          color: "black",
          name: "报名成功",
          unread: 0,
          path:'signed'
        },
        {
          icon: "squarecheck",
          color: "black",
          name: "已完成",
          unread: 3,
          path:'success'
        },
        {
          icon: "refund",
          color: "black",
          name: "退款/取消",
          unread: 0,
          path:'refund'
        },
      ],
    };
  },
};
</script>

<style>
</style>