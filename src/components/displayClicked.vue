<template>
  <div v-if="users !== undefined">
    <div v-for="user in users" :key="user[`id`]">
      <button>{{ user[`name`] }}</button>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$root.$on(`user_clicked`, this.new_function);
  },
  methods: {
    new_function(random_user) {
      for (let i = 0; i < this.users.length; i++) {
        if (this.users[i][`id`] !== random_user[i][`id`]) {
          this.users.push(random_user[i]);
        }
      }
    },
  },
  data() {
    return {
      users: [],
    };
  },
};
</script>

<style scoped></style>
