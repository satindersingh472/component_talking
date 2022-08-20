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
        if (this.users[`id`].includes(random_user[`id`]) === false){
          this.users.push(random_user);

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
