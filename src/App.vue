<template>
  <div class="fonte container">
    <dataBindingVue></dataBindingVue>
    <diretivasFocusVue></diretivasFocusVue>
    <eventosMetodosVue></eventosMetodosVue>
    <novaSyntaxsEAntigaVue></novaSyntaxsEAntigaVue>
    <lifeCycleHooksVue></lifeCycleHooksVue>
  </div>
</template>

<script>
import dataBindingVue from "./components/data-binding.vue";
import diretivasFocusVue from "./components/diretivas-focus.vue";
import eventosMetodosVue from "./components/eventos-metodos.vue";
import lifeCycleHooksVue from './components/life-cycle-hooks.vue';
import novaSyntaxsEAntigaVue from "./components/nova-syntaxs-e-antiga.vue";

export default {
  components: {
    dataBindingVue,
    diretivasFocusVue,
    eventosMetodosVue,
    novaSyntaxsEAntigaVue,
    lifeCycleHooksVue
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@800&display=swap');

.container {
  display: flex;
  justify-content: space-around; /* Distribui os componentes com espaço igual entre eles */
  align-items: flex-start; /* Alinha os componentes no início do container */
  flex-wrap: wrap; /* Permite que os componentes quebrem a linha se o espaço não for suficiente */
}

.fonte {
  font-family: "Inter", sans-serif;
  font-optical-sizing: auto;
  font-weight: 800;
  font-style: normal;
  font-variation-settings: "slnt" 0;
}
</style>
