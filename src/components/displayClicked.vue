<template>
   <div @user_clicked="new_function">
          <h2 v-if="the_word !== undefined">no error</h2>
          <h2 v-else-if="the_word === undefined">there is nothing to show </h2>
  </div>
</template>

<script>
export default {
  methods: {
    new_function(user) {
      this.the_word = user;
    },
  },
  data() {
    return {
      the_word: undefined
    };
  },
};
</script>

<style scoped></style>
