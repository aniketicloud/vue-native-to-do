<template>
  <view class="container">
    <button :onPress="handleBtnClickCount" :title="btnTitle"></button>
    <text class="text-container">{{ btnClickCount }}</text>
  </view>
</template>

<script>
export default {
  data() {
    return {
      btnTitle: "Touch Me",
      btnClickCount: 0,
    };
  },

  methods: {
    handleBtnClickCount() {
      this.btnClickCount++;
    },
  },
};
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
