<template>
  <div class="exercise-3">
    <GreyCard>
      <template v-slot:body>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Facere est
          cumque quae adipisci autem itaque? Officia, cum porro nam quam, maxime
          cumque repellat impedit omnis neque explicabo reiciendis provident
          doloribus?
        </p>
      </template>

      <template v-slot:title>
        Titre
      </template>
    </GreyCard>
  </div>
</template>

<script>
import GreyCard from "./GreyCard";

export default {
  name: "Exercise3",
  components: { GreyCard },
};
</script>

<style lang="stylus" scoped>
@import '../../theme.styl';

.exercise-3 {
  color: $grey;
}
</style>
