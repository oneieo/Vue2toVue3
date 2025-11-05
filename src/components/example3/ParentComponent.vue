<!-- ParentComponent.vue -->
<!-- <template>
  <div>
    <ChildComponent
        :message="parentMessage"
        @custom-event="handleEvent"
    />
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  name: "E05ParentComponent",
  data() {
    return {
      parentMessage: 'Hello from parent'
    };
  },
  methods: {
    handleEvent(payload) {
      console.log(payload);
    }
  },
  components: {
    ChildComponent
  }
};
</script> -->

<template>
  <div>
    <ChildComponent :message="parentMessage" @custom-event="handleEvent" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";

const parentMessage = ref("Hello from parent");

const handleEvent = (payload) => {
  console.log(payload);
};
</script>
