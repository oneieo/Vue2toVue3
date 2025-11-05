<template>
  <E05ParentComponent />
</template>

<script lang="ts">
import { defineComponent } from "vue";
//import E01Instance from "@/components/example1/E-01-instance.vue";
//import E02Reactive from "@/components/example1/E-02-reactive.vue";
//import E03Binding from "@/components/example1/E-03-binding.vue";
//import E04Directives from "@/components/example2/E-04-directives.vue";
import E05ParentComponent from "@/components/example3/ParentComponent.vue";

export default defineComponent({
  name: "App",
  components: {
    E05ParentComponent,
  },
});
</script>

<style></style>
