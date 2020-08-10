<template>
  <div class="user-card">
    <h2>{{ name }}</h2>
    <span>Mon id est : {{ id }}</span>
    <p>{{ email }}</p>
    <p v-if="premium">Je suis premium ! 🔱</p>
  </div>
</template>

<script>
export default {
  name: "UserCard",

  props: {
    id: {
      type: Number,
      default: 0,
    },
    name: {
      type: String,
      required: true,
    },
    premium: {
      type: Boolean,
      required: true,
    },
    email: {
      type: String,
      required: false,
    },
  },

  //   computed: {
  //     fullName() {
  //       return `${this.firstname} ${this.lastname}`;
  //     },
  //   },
};
</script>

<style>
.user-card {
  width: 300px;
  margin: 20px;
  border: 1px solid red;
  border-radius: 20px;
  /* color: grey; */
  color: #fff;
}
</style>
