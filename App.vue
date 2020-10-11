<template>
  <view class="container">
    <app-status-bar color="#ffce00" />
    <app-main-header title="to-do-app"></app-main-header>
    <app-new-to-do :todos="todos"></app-new-to-do>
    <app-to-do-list :todos="todos"></app-to-do-list>
  </view>
</template>

<script>
import StatusBar from "./components/status-bar/StatusBar";
import MainHeader from "./components/mainheader/MainHeader";
import NewToDo from "./components/new-to-do/NewToDo";
import ToDoList from "./components/to-do-list/ToDoList";

export default {
  components: {
    appStatusBar: StatusBar,
    appMainHeader: MainHeader,
    appNewToDo: NewToDo,
    appToDoList: ToDoList,
  },

  data() {
    return {
      todos: [
        {
          id: 0,
          title: "Complete Vue native",
          done: false,
        },
        {
          id: 1,
          title: "Revise your Chinese",
          done: false,
        },
      ],
    };
  },
};
</script>

<style>
.container {
  background-color: white;
  flex: 1;
}
</style>
