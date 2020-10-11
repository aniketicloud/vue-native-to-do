<template>
  <view class="inputContainer">
    <text-input class="input" v-model="newTodoText"></text-input>
    <touchable-opacity class="add-btn" :onPress="newTodo">
      <text class="btn-text">ADD</text>
    </touchable-opacity>
  </view>
</template>

<script>
export default {
  data() {
    return {
      newTodoText: "",
    };
  },

  methods: {
    newTodo() {},
  },
};
</script>

<style scoped>
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
