<template>
  <div id="app"><BaseInput /> <BaseInput /> <PasswordField /></div>
</template>

<script>
import BaseInput from "./components/BaseInput";
import PasswordField from "./components/PasswordField";
export default {
  name: "App",
  components: { BaseInput, PasswordField },
};
</script>

<style>
#app {
  height: 100vh;
  width: 100vw;
  background: beige;
}
body {
  margin: 0px;
}
</style>
