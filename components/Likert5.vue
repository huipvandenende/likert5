<template>
  <v-card class="text-center mt-4">
    <div>{{ question }}</div>
    <v-rating
      v-model="rating"
      background-color="indigo lighten-3"
      clearable
      color="red"
      large
    ></v-rating>
    <span class="font-weight-bold">
        {{ displayRating }}
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
      rating: null as number | null,
    };
  },
  computed: {
    displayRating(): string {
      if (this.rating === null || this.rating === 0) {
        return 'Not applicable';
      }
      return this.rating.toString();
    }
  },
});
</script>
