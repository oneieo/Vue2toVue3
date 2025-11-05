<!-- ChildComponent.vue -->
<!-- <template>
  <div>
    <p>{{ message }}</p>
    <button @click="$emit('custom-event', 'Hello from child')">Send Event</button>
  </div>
</template>

<script>
export default {
  props: ['message']
};
</script> -->

<template>
  <div>
    <p>{{ message }}</p>
    <button @click="emit('custom-event', 'Hello from child')">
      Send Event
    </button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

defineProps({
  message: String,
});

const emit = defineEmits(["custom-event"]);
</script>
