<template>
  <div id="app">
    <display-users v-for="user in users" :key="user[`id`]" :user="user" >
    </display-users>
<display-clicked></display-clicked>
  </div>
</template>

<script>
import DisplayClicked from "@/components/displayClicked.vue";
import DisplayUsers from "@/components/displayUsers.vue"
export default {
  name: "App",
  components: {
    DisplayUsers,
    DisplayClicked,
  },
  data() {
    return {
      users: [
        {
          name: `sat`,
          id: 1,
          status: `logged_in`,
        },
        {
          name: `nav`,
          id: 2,
          status: `logged_out`,
        },
        {
          name: `nav`,
          id: 3,
          status: `revoked`,
        },
      ],
    };
  },
};
</script>

<style></style>
