<!-- <template>
  <div>{{ fullName }}</div>
</template>

<script>
export default {
  name: "E02Reactive",
  data() {
    return {
      firstName: "Kyungsu",
      lastName: "Lee"
    };
  },
  mounted() {
    setTimeout(() => {
      this.firstName = "KSL";
    }, 2000);
  },
  computed: {
    fullName() {
      return this.firstName + " " + this.lastName;
    }
  }
};
</script> -->

<template>
  <div>{{ fullName }}</div>
</template>

<script setup>
import { ref, computed, onMounted } from "vue";

const firstName = ref("Kyungsu");
const lastName = ref("Lee");

const fullName = computed(() => {
  return firstName.value + " " + lastName.value;
});

onMounted(() => {
  setTimeout(() => {
    firstName.value = "KSL";
  }, 2000);
});
</script>
