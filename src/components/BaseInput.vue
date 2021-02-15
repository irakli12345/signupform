<template>
  <div>
    <input type="text" />
  </div>
</template>

<script>
export default {
  name: "BaseInput",
  props: {},
  methods: {},
};
</script>

<style scoped>
div {
  width: 80%;
  margin-left: auto;
  margin-right: auto;
  margin-top: 1rem;
}
input {
  height: 2rem;
  border-radius: 0.5rem;
  border: 0;
  width: 100%;
}
</style>
