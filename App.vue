<template>
  <view class="container">
    <view class="btn-container">
      <button title="show A" :on-press="() => handleBtnClick('A')" />
      <button title="show B" :on-press="() => handleBtnClick('B')" />
      <button title="show C" :on-press="() => handleBtnClick('C')" />
    </view>
    <view>
      <text v-if="type === 'A'"> A </text>
      <text v-else-if="type === 'B'"> B </text>
      <text v-else-if="type === 'C'"> C </text>
      <text v-else> NOT A/B/C </text>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      type: Number,
    };
  },

  methods: {
    handleBtnClick(type) {
      this.type = type;
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
