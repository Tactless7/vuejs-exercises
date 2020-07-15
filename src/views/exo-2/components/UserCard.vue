<template>
  <div class="user-card">
    <h2 :class="{'premium': user.premium === true}">{{ fullName(user.firstname, user.lastname) }}</h2>
    <img :src="`https://i.picsum.photos/id/${user.id}/80/80.jpg`" />
    <!-- <img :src="`https://i.picsum.photos/id/${getRandomNumber()}/80/80.jpg`" /> -->
    <p>email: {{ user.email }}</p>
    <p>mot de passe :{{ user.password }}</p>

    <!-- J'utilise une classe dynamique qui donne une couleur 
    de fond quand la prop id a une valeur paire-->
    <button @click="togglePremium(user)" :class="{blue: id % 2 === 0}">
      <span v-if="user.premium === true">Ne plus être Premium</span>
      <span v-else>Devenir Premium</span>
    </button>
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
    id: {
      type: Number,
      required: true,
    },
  },

  methods: {
    togglePremium(object) {
      object.premium = !object.premium;
    },
    fullName: function(first, last) {
      return `${first} ${last}`;
    },
    getRandomNumber: function() {
      return Math.floor(Math.random() * Math.floor(100));
    },
  },
};
</script>

<style lang="stylus" scoped>
@import '../../../theme.styl';

.user-card {
  border: $grey solid 1px;
  width: 250px;
  height: 350px;
  margin: 20px;

  .premium {
    color: green;
  }

  .blue {
    background-color: blue;
  }
}
</style>