<template>
  <div>
    <label for="textInput"> {{ label + " : " }}</label>
    <input type="text" id="textInput" />
    <p v-if="error">Please Enter Valid {{ label }}</p>
  </div>
</template>

<script>
export default {
  name: "BaseInput",
  data: function() {
    return {
      error: false,
    };
  },
  props: {
    label: { type: String, required: true },
  },
  methods: {},
};
</script>

<style scoped>
div {
  width: 80%;
  margin-left: auto;
  margin-right: auto;
  margin-top: 0.5rem;
}
input {
  height: 2rem;
  border-radius: 0.5rem;
  border: 0;
  width: 65%;
  float: right;
}
label {
  width: 30%;
}
@media screen and (min-width: 1200px) {
  input {
    width: 70%;
  }
}
</style>
