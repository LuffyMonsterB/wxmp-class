<template>
  <view class="cu-list grid col-3  no-border" style="background-color:#f8f8f8">
    <view class="cu-item" v-for="(item, index) in classList" :key="index">
      <view :class="['cuIcon-' + item.icon, 'text-' + item.color]"> </view>
      <text>{{ item.name }}</text>
    </view>
  </view>
</template>

<script>
export default {
  name: "Classification",
  data() {
    return {
      classList: [
        {
          icon: "cardboardfill",
          color: "red",
          name: "分类1",
          type:"1"
        },
        {
          icon: "recordfill",
          color: "orange",
          name: "分类2",
          type:"2",
        },
        {
          icon: "picfill",
          color: "yellow",
          name: "分类3",
          type:"3"
        },
        {
          icon: "noticefill",
          color: "olive",
          name: "分类4",
          type:"4"
        },
        {
          icon: "upstagefill",
          color: "cyan",
          name: "分类5",
          type:"5"
        },
        {
          icon: "clothesfill",
          color: "blue",
          name: "分类6",
          type:"6"
        }
      ],
    };
  },
};
</script>

<style></style>
