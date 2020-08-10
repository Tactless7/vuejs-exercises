<template>
  <div class="exercise-2">
    <GreyCard v-for="utilisateur in utilisateurs" :key="utilisateur.id">
      <UserCard
        :id="utilisateur.id"
        :email="utilisateur.email"
        :name="fullName(utilisateur.firstname, utilisateur.lastname)"
        :premium="utilisateur.premium"
      />

      <!-- <UserCard :email="email" />
      <UserCard email="toto@gmail.com" /> -->
    </GreyCard>
  </div>
</template>

<script>
import { users } from "./data.js";
import UserCard from "./UserCard";
import GreyCard from "../exo-3/GreyCard";

export default {
  name: "Exercise2",

  components: { UserCard, GreyCard },

  data() {
    return {
      utilisateurs: users,
      email: "tutu&gmail.com",
    };
  },
  methods: {
    fullName(first, last) {
      return `${first} ${last}`;
    },
  },
};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-2 {
  // color: $grey;
  color: #fff;
}
</style>
