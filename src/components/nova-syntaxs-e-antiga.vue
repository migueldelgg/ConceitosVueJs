<template>
  <div>
    <h1 class="h1color">{{ state.tituloObj }}</h1>
    <h2>Minha lista de tarefas!</h2>
    <button @click="handlerShowHideList">Ver minha lista!</button>
    <br />
    <input type="text" @keyup.enter="addTask" v-focus v-model="state.currentTask" />

    <ul v-if="state.showList">
      <li
        v-for="(task, index) in state.tasks"
        @dblclick="complete(task)"
        :key="`${task.name}-${index}`"
        class="task-item"
        :class="{
          'line-through': task.isDone,
        }"
      >
        {{ task.name }}
        <button @click="remove(task)">&times;</button>
      </li>
    </ul>
    <p v-else>Lista de tarefas escondidas</p>
  </div>
</template>

<script>
import { reactive } from 'vue';

const focus = {
  mounted(el) {
    el.focus();
  },
};

export default {
  directives: {
    focus,
  },
  setup() {
    const state = reactive({
      tituloObj: 'Novas syntaxs e antigas',
      currentTask: '',
      showList: false,
      tasks: [
        { name: 'Fazer curso de vue', isDone: false },
      ],
    });

    function addTask() {
      state.tasks.push({
        name: state.currentTask,
        isDone: false,
      });
      state.currentTask = '';
    }

    function remove(task) {
      state.tasks = state.tasks.filter((t) => t.name !== task.name);
    }

    function complete(task) {
      state.tasks = state.tasks.map((t) => {
        if (t.name === task.name) {
          return { ...t, isDone: !t.isDone };
        }
        return { ...t };
      });
    }

    function handlerShowHideList() {
      state.showList = !state.showList;
    }

    return {
      state,
      addTask,
      remove,
      complete,
      handlerShowHideList,
    };
  },
};
</script>

<style scoped>
.line-through {
  text-decoration: line-through;
}

.task-item {
  cursor: pointer;
}

.h1color {
  color: rgb(90, 100, 242);
}
</style>
