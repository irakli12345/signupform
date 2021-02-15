<template>
  <div class="passwordWrapper">
    <input type="text" />
    <span></span>
    <div id="conditions">
      <li>One lowercase character</li>
      <li>One uppercase character</li>
      <li>One number</li>
      <li>One special character</li>
      <li>8 characters minimum</li>
    </div>
  </div>
</template>

<script>
export default {
  name: "PasswordField",
  props: {},
  methods: {},
};
</script>

<style scoped>
.passwordWrapper {
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
#conditions {
  display: flex;
  flex-flow: row wrap;
  list-style: none;
}
li {
  flex-basis: 50%;
}
li::before {
  content: "\2022";
  color: rgb(129, 34, 34);
  font-weight: bold; /* If you want it to be bold */
  display: inline-block; /* Needed to add space between the bullet and the text */
  width: 1em; /* Also needed for space (tweak if needed) */
  margin-left: -1em; /* Also needed for space (tweak if needed) */
  font-size: 24px;
  text-align: center;
}
span {
  background-color: green;
  display: block;
  margin-top: 1rem;
  height: 0.8rem;
}
</style>
