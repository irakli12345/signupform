<template>
  <div id="app">
    <div id="formWrapper">
      <FormHeading />
      <BaseInput />
      <BaseInput />
      <PasswordField />
    </div>
  </div>
</template>

<script>
import FormHeading from "./components/FormHeading";
import BaseInput from "./components/BaseInput";
import PasswordField from "./components/PasswordField";
export default {
  name: "App",
  components: { BaseInput, PasswordField, FormHeading },
};
</script>

<style>
#app {
  height: 100vh;
  width: 100vw;
  background: beige;
  display: flex;
  justify-content: center;
  align-content: center;
}
body {
  margin: 0px;
}
#formWrapper {
  width: 30%;
  background: rgba(111, 236, 236, 0.651);
  margin: auto;
  display: flex;
  flex-direction: column;
  padding: 1rem;
  border-radius: 2rem;
  height: 50%;
}
</style>
