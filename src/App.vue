<template>
  <div id="app">
    <div id="formWrapper">
      <FormHeading />
      <BaseInput :label="'E-Mail'" />
      <BaseInput :label="'Username'" />
      <PasswordField />
      <Button />
    </div>
  </div>
</template>

<script>
import FormHeading from "./components/FormHeading";
import BaseInput from "./components/BaseInput";
import PasswordField from "./components/PasswordField";
import Button from "./components/Button";
export default {
  name: "App",
  components: { BaseInput, PasswordField, FormHeading, Button },
};
</script>

<style>
p {
  font-size: 14px;
}
#app {
  height: 100vh;
  width: 100vw;
  background: beige;
  display: flex;
  justify-content: center;
  align-content: center;
  font-family: "Poppins", sans-serif;
}
body {
  margin: 0px;
}
#formWrapper {
  width: 80%;
  background: rgba(111, 236, 236, 0.651);
  margin: auto;
  display: flex;
  flex-direction: column;
  padding: 1rem;
  border-radius: 2rem;
  height: 80%;
}
@media screen and (min-width: 500px) {
  #formWrapper {
    width: 60%;

    height: 70%;
  }
}
@media screen and (min-width: 800px) {
  #formWrapper {
    width: 40%;
    height: 70%;
  }
}
@media screen and (min-width: 1200px) {
  #formWrapper {
    width: 30%;

    height: 60%;
  }
}
label {
  font-size: 14px;
}
</style>
