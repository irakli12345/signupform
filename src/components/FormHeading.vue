<template>
  <div>
    <div class="imgAndHeading">
      <img src="https://image.flaticon.com/icons/png/512/2037/2037710.png" />
      <h1>Form Heading Join Us</h1>
    </div>
    <p>
      There are many variations of passages of Lorem Ipsum available, but the
      majority have suffered alteration in some form, by injected humour.
    </p>
  </div>
</template>

<script>
export default {
  name: "FormHeading",
};
</script>

<style scoped>
div {
  width: 100%;
  margin-left: auto;
  margin-right: auto;
}
img {
  width: 20%;
  height: 20%;
  display: inline;
}
h1 {
  display: inline;
}
.imgAndHeading {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
