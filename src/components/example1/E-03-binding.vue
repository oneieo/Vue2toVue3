<!-- <template>
  <div>
    <input v-model="message" />
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  name: "E03Binding",
  data() {
    return {
      message: "Hello Vue"
    };
  }
};
</script> -->

<template>
  <div>
    <input v-model="message" />
    <p>{{ message }}</p>
  </div>
</template>

<script setup>
import { ref } from "vue";

const message = ref("Hello Vue");
</script>
