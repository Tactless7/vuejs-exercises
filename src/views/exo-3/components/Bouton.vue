<template>
  <div class="bouton">
    <button v-bind:class="{ 'avec-erreur': hasError, 'vert': green }">{{ title }}</button>
    <p v-if="hasError">{{ error }}</p>
  </div>
</template>

<script>
export default {
  name: 'Bouton',
  props: {
    hasError: {
      type: Boolean,
      default: false,
    },
    error: {
      type: String,
    },
    green: {
      type: Boolean,
      default: false,
    },
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="stylus" scoped>
@import '../../../theme.styl';

.avec-erreur {
  border: solid 1px red;
}

.vert {
  background-color: green;
  color: white;
}
</style>