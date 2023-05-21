<template>
  <view class="cu-bar tabbar bg-white">
    <view
      v-for="(item, index) in pageList"
      :key="index"
      :class="[
        'action',
        item.page === activePage ? activeClass : inactiveClass,
        item.isCenter?'add-action':''
      ]"
      @click="changePageTo(item.page)"
    >
      <button :class="[item.icon,'bg-cyan','shadow','cu-btn']" v-if="item.isCenter"></button>
      <view :class="item.icon" v-else></view> {{ item.text }}
    </view>
  </view>
</template>

<script>
export default {
  name: "Tabbar",
  props: ["pageList", "activePage"],
  data() {
    return {
      activeClass: "text-cyan",
      inactiveClass: "text-gray",
    };
  },
  methods: {
    changePageTo(page) {
      this.$emit("changePageTo", page);
    },
  },
};
</script>

<style></style>
