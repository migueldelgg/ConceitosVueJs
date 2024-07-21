<template>
  <div>
    <h1>Diretivas</h1>
    <h2>Minha lista de tarefas!</h2>
    <button @click="() => (showList = !showList)">Ver minha lista!</button>
    <br />
    <input type="text" v-focus />

    <ul v-if="showList">
      <li v-for="(task, index) in tasks" :key="`${task.name}-${index}`">
        {{ task.name }}
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
    showList: false,
    tasks: [{ name: "Fazer o Curso", isDone: false }],
  }),
};
</script>