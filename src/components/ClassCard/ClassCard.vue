<template>
  <view class="cu-card case">
  <view class="cu-item item-shadow">
    <view class="image">
      <image :src="classInfo.imgUrl" mode="widthFix"></image>
      <view class="cu-tag bg-red">{{classInfo.tag}}</view>
      <view class="cu-bar bg-shadeBottom">
        <text class="text-cut">{{classInfo.description}}</text>
      </view>
    </view>
    <view class="cu-list">
      <view class="cu-item flex justify-between">
        <view class="content padding-xs" style="width:75%">
          <view class="text-black text-lg margin-bottom-xs text-cut">{{classInfo.title}}</view>
          <view class="text-gray text-sm flex justify-start">
            <view class="cuIcon-time margin-right-xs">{{classInfo.time}}</view>
            <view class="cuIcon-location margin-right-xs">{{classInfo.location}}</view>
            <view class="cuIcon-friend">{{classInfo.member}}</view>
          </view>
        </view>
        <view class="flex align-center justify-end">
          <text class="text-price text-red text-xl text-cut padding-xs">{{classInfo.price}}</text>
        </view>
      </view>
    </view>
  </view>

</view>
</template>

<script>
export default {
  name:"ClassCard",
  props:['classInfo']
}
</script>

<style>
.item-shadow{
box-shadow: 2rpx 2rpx 6rpx #bbbbbb;
}
</style>