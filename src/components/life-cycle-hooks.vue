<template>
  <div>
    <h1>Lifecycle Hooks</h1>
    <a
      href="https://v3.vuejs.org/guide/composition-api-lifecycle-hooks.html#lifecycle-hooks"
    >
      Documentacao</a
    >
  </div>
</template>

<script>
import { onMounted } from "vue";
/*
export default{
    mounted(){
        console.log('foi montado!')
    }
}*/

export default {
  setup() {
    onMounted(() => {
      console.log("Foi montado com composion.api");
      console.log(
        "https://v3.vuejs.org/guide/composition-api-lifecycle-hooks.html#lifecycle-hooks"
      );
    });
  },
};
</script>