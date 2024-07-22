<template>
  <div>
    <dataBindingVue></dataBindingVue>
    <p class="p">----------------------------------</p>
    <diretivasFocusVue></diretivasFocusVue>
    <p class="p">----------------------------------</p>
    <eventosMetodosVue></eventosMetodosVue>
  </div>
</template>

<script>
import dataBindingVue from "./components/data-binding.vue";
import diretivasFocusVue from "./components/diretivas-focus.vue";
import eventosMetodosVue from "./components/eventos-metodos.vue";

export default {
  components: {
    dataBindingVue,
    diretivasFocusVue,
    eventosMetodosVue
  }
}
</script>

<style scoped>
.p {
  padding: 35px;
}
</style>
