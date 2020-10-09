<template>
  <view class="container">
    <app-status-bar color="#ffce00" />
    <app-main-header title="to-do-app"></app-main-header>

    <view class="inputContainer">
      <text-input class="input" v-model="newTodoText"></text-input>
      <touchable-opacity class="add-btn" :onPress="newTodo">
        <text class="btn-text">ADD</text>
      </touchable-opacity>
    </view>
  </view>
</template>

<script>
import StatusBar from "./components/status-bar/StatusBar";
import MainHeader from "./components/mainheader/MainHeader";

export default {
  data() {
    return {
      newTodoText: "",
    };
  },
  components: {
    appStatusBar: StatusBar,
    appMainHeader: MainHeader,
  },
  methods: {
    newTodo() {},
  },
};
</script>

<style>
.container {
  background-color: white;
  flex: 1;
}

.inputContainer {
  width: 100%;
  flex-direction: row;
  justify-content: center;
  align-self: stretch;
}

.input {
  flex: 1;
  height: 35px;
  background-color: #f3f3f3;
  font-size: 18px;
  color: #888888;
}

.add-btn {
  width: 100px;
  height: 35px;
  background-color: #ffce00;
  justify-content: center;
  align-items: center;
}

.btn-text {
  font-size: 18px;
  font-weight: 700;
}
</style>
