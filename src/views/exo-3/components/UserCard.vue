<template>
  <div class="user-card">
    <h2>{{ fullName(user.firstname, user.lastname) }}</h2>
    <img :src="`https://picsum.photos/id/${getRandomNumber() + 1}/70/70`" alt />
    <p>{{ user.email }}</p>
    <p>{{ user.password }}</p>
  </div>
</template>

<script>
export default {
  name: 'UserCard',

  props: {
    user: {
      type: Object,
      required: true,
    },
  },

  methods: {
    fullName(first, last) {
      return `${first} ${last}`;
    },
    getRandomNumber() {
      return Math.floor(Math.random() * Math.floor(100));
    },
  },
};
</script>

<style>
</style>