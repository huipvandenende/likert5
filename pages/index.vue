<template>
  <div>
    <form>
      <Likert5
        v-for="(question, index) in questions"
        :key="index"
        :question="question"
      />
    </form>
  </div>
</template>

<script setup lang="ts">
import {ref} from 'vue';

const questions = ref([
  'How much do you like this template?',
  'How user-friendly do you find the interface?',
  'How satisfied are you with the performance?',
  'How likely are you to recommend this to others?',
  'How do you rate the overall quality?'
]);
</script>
