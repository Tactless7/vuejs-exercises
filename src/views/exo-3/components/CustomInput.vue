<template>
  <div class="bouton">
    <input type="text" :class="{error: hasError}" />
    <p v-if="hasError">{{ error }}</p>
  </div>
</template>

<script>
export default {
  name: 'CustomInput',
  props: {
    error: {
      type: String,
      required: false,
    },
    hasError: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="stylus" scoped>
@import '../../../theme.styl';

.bouton input {
  width: 100px;
  height: 30px;
  border-radius: 20px;

  &.error {
    border: solid red 1px;
  }
}
</style>