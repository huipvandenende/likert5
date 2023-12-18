<template>
  <v-card class="text-center">
    <div>{{ question }}</div>
    <v-rating
      v-model="rating"
      background-color="indigo lighten-3"
      clearable
      color="red"
      large
    ></v-rating>
    <span class="font-weight-bold">
        {{ rating }}
      </span>
  </v-card>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  props: {
    question: String,
  },
  data() {
    return {
      rating: 0,
    };
  },
});
</script>
