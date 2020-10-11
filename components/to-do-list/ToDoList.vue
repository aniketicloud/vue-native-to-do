<template>
  <view>
    <text class="todolist" v-for="todo in todos" :key="todo.id">
      <touchable-opacity :on-press="() => toggleDone(todo.id)">
        <text class="todo-text done" v-if="todo.done">{{ todo.title }}</text>
        <text class="todo-text" v-else>{{ todo.title }}</text>
      </touchable-opacity>

      <touchable-opacity
        class="remove-btn"
        :on-press="() => removeTodo(todo.id)"
      >
        <text class="remove-btn-text">Remove</text>
      </touchable-opacity>
    </text>
  </view>
</template>

<script>
export default {
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

  methods: {
    toggleDone() {},
    removeTodo() {},
  },
};
</script>

<style scoped>
.todolist {
  flex-direction: row;
  justify-content: space-between;
  padding: 15px;
}

.todo-text {
  font-size: 18px;
}

.done {
  color: chartreuse;
}

.remove-btn-text {
  font-size: 18px;
  color: crimson;
}
</style>
