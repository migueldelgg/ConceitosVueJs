<template>
  <div>
    <h1>Diretivas</h1>
    <h2>Minha lista de tarefas!</h2>
    <button @click="handlerShowHideList">Ver minha lista!</button>
    <br />
    <input 
      type="text" 
      @keyup.enter="addTask"
      v-focus 
      v-model="currentTask" />

    <ul v-if="showList">
      <li
        v-for="(task, index) in tasks"
        @dblclick="complete(task)"
        :key="`${task.name}-${index}`"
        class="task-item"
        :class="{
          'line-through': task.isDone
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
const focus = {
  mounted(el) {
    el.focus();
  },
};

export default {
  directives: {
    focus,
  },
  name: "DiretivasVue",
  data: () => ({
    currentTask: '',
    showList: false,
    tasks: [{ name: "Fazer o Curso", isDone: false }],
  }),
  methods: {
    addTask(){
      this.tasks.push({
        name: this.currentTask,
        isDone: false
      })
      this.currentTask = ''
    },
    remove(task) {
      this.tasks = this.tasks.filter((t) => t.name !== task.name);
    },
    complete(task) {
      this.tasks = this.tasks.map((t) => {
        if (t.name === task.name) {
          return { ...t, isDone: !t.isDone };
        }
        return { ...t };
      });
    },
    handlerShowHideList() {
      this.showList = !this.showList;
    },
  },
};
</script>

<style scoped>
  .line-through{
    text-decoration: line-through;
  }

  .task-item{
    cursor: pointer;
  }

</style>