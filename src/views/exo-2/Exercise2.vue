<template>
  <div class="exercise-2">
    <div class="user-card" v-for="user in users" :key="user.id">
      <UserCard :user="user" :id="user.id" />
    </div>
  </div>
</template>

<script>
import { users } from './data.js';
import UserCard from './components/UserCard';

export default {
  name: 'Exercise2',
  components: { UserCard },
  data: function() {
    return {
      users: users,
    };
  },
};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-2 {
  color: $grey;
  display: flex;
  flex-wrap: wrap;
}
</style>
