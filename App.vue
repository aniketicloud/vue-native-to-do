<template>
  <view class="container">
    <app-status-bar color="#ffce00" />
    <app-main-header title="to-do-app"></app-main-header>
  </view>
</template>

<script>
import StatusBar from "./components/status-bar/StatusBar";
import MainHeader from "./components/mainheader/MainHeader";

export default {
  components: {
    appStatusBar: StatusBar,
    appMainHeader: MainHeader,
  },
};
</script>

<style>
.container {
  background-color: bisque;
  flex: 1;
}
</style>
