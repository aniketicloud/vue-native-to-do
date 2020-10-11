<template>
  <view class="container">
    <app-status-bar color="#ffce00" />
    <app-main-header title="to-do-app"></app-main-header>
    <app-new-to-do></app-new-to-do>
  </view>
</template>

<script>
import StatusBar from "./components/status-bar/StatusBar";
import MainHeader from "./components/mainheader/MainHeader";
import NewToDo from "./components/new-to-do/NewToDo";

export default {
  components: {
    appStatusBar: StatusBar,
    appMainHeader: MainHeader,
    appNewToDo: NewToDo,
  },
};
</script>

<style>
.container {
  background-color: white;
  flex: 1;
}
</style>
