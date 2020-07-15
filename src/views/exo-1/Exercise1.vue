<template>
  <div class="exercise-1">
    <h1>Bienvenue, {{ firstname }} {{ lastname }} !</h1>
    <h1>Bienvenue, {{ firstname + ' ' + lastname }} !</h1>
    <h1>Bienvenue, {{ `${firstname} ${lastname}` }} !</h1>

    <p>Entre ici ton prénom :</p>
    <input type="text" v-model="firstname" />
    <p>Vous vous appelez {{ firstname }}</p>

    <p>Entrez ici votre âge :</p>
    <input type="nombre" v-model="age" />

    <div v-if="age !== 0">
      <p v-if="age < 18">Vous êtes mineur</p>
      <p v-else-if="age > 18">Vous êtes majeur</p>
      <p v-else>Vous êtes tout juste majeur</p>
    </div>

    <p v-if="age !== 0">Vous êtes né en : {{ 2020 - age }}</p>
  </div>
</template>

<script>
export default {
  name: 'Exercise1',
  data() {
    return {
      firstname: 'Juliane',
      lastname: 'Blier',
      age: 0,
    };
  },
};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-1 h1 {
  color: $grey;
}
</style>
