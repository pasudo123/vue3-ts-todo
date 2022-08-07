<template>
  <div class="home">
    <div class="nameWrapper">Todo List</div>
    <el-input v-model="input" placeholder="오늘 할 일을 입력하자" @keyup.enter="addTodo">
      <template #append>
        <el-button @click="addTodo">등록</el-button>
      </template>
    </el-input>
    <div class="tableWrapper">
      <el-table :data="todos" stripe style="width: 100%">
        <el-table-column prop="text" label="Todo" align="center"/>
        <el-table-column fixed="right" label="Action" align="center" width="90">
          <template #default="scope">
            <el-button link type="primary" size="small" @click="deleteTodo(scope.$index)">삭제</el-button>
          </template>
        </el-table-column>
      </el-table>
    </div>
  </div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import Todo from '@/types/Todo'

export default defineComponent({
  components: {},
  setup () {
    const todos = ref<Todo[]>([
      { text: 'sample todo' }
    ])
    return { todos }
  },
  data: () => {
    return {
      input: ''
    }
  },
  methods: {
    addTodo () {
      const currentTodo: Todo = {
        text: this.input
      }
      this.todos.push(currentTodo)
      this.input = ''
    },

    deleteTodo (index: number) {
      this.todos.splice(index, 1)
    }
  }
})
</script>
