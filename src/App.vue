<template>
  <div class="fonte">
    <dataBindingVue></dataBindingVue>
    <p class="p">----------------------------------</p>
    <diretivasFocusVue></diretivasFocusVue>
    <p class="p">----------------------------------</p>
    <eventosMetodosVue></eventosMetodosVue>
    <p class="p">----------------------------------</p>
    <novaSyntaxsEAntigaVue></novaSyntaxsEAntigaVue>
    <p class="p">----------------------------------</p>
  </div>
</template>

<script>
import dataBindingVue from "./components/data-binding.vue";
import diretivasFocusVue from "./components/diretivas-focus.vue";
import eventosMetodosVue from "./components/eventos-metodos.vue";
import novaSyntaxsEAntigaVue from './components/nova-syntaxs-e-antiga.vue';

export default {
  components: {
    dataBindingVue,
    diretivasFocusVue,
    eventosMetodosVue,
    novaSyntaxsEAntigaVue
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@800&display=swap');

.p {
  padding: 35px;
}

.fonte{
  font-family: "Inter", sans-serif;
  font-optical-sizing: auto;
  font-weight: 800;
  font-style: normal;
  font-variation-settings:
    "slnt" 0;
}
</style>
