<template>
  <div class="exercise-3">
    <Bouton
      @click.native="echec = !echec"
      :title="'Cliquez-moi'"
      :hasError="echec"
      :error="'Il y a une erreur'"
    />
  </div>
</template>

<script>
import Bouton from './components/Bouton';

export default {
  name: 'Exercise3',

  components: { Bouton },

  data() {
    return {
      echec: false,
    };
  },
};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-3 {
  color: $grey;
}
</style>
