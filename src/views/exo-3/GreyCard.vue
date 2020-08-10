<template>
  <div class="grey-card">
    <h4 class="titre">
      <slot name="title" />
    </h4>
    <slot name="body" />
  </div>
</template>

<script>
export default {
  name: "GreyCard",
};
</script>

<style scoped>
.grey-card {
  width: 300px;
  height: 300px;
  background: grey;
  border-radius: 30px;
  box-shadow: 10px 10px 10px;
  padding: 10px;
}

.titre {
  color: red;
  font-size: 30px;
}
</style>
