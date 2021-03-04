<template>
  <div class="passwordWrapper">
    <label for="password">Password : </label>
    <input type="password" id="password" @keyup="checkPassword" />
    <span></span>
    <div id="conditions">
      <li id="lowercase">One lowercase character</li>
      <li id="uppercase">One uppercase character</li>
      <li id="number">One number</li>
      <li id="special">One special character</li>
      <li id="length">8 characters minimum</li>
    </div>
  </div>
</template>

<script>
export default {
  name: "PasswordField",
  data: function() {
    return {
      conditions: {
        lowercase: false,
        uppercase: false,
        number: false,
        special: false,
        length: false,
      },
    };
  },
  props: {},
  methods: {
    checkPassword: function(e) {
      let upperCaseRegExp = /.*[A-Z].*/;
      let lowerCaseRegExp = /.*[a-z].*/;
      let specialSymbolsRegExp = /[-!$%^&*()_+|~=`{}\]:;<>?,.@#]/;
      // let digitRegExp = /.*[0-9].*/;
      if (upperCaseRegExp.test(e.target.value)) {
        this.conditions.uppercase = true;
      } else if (lowerCaseRegExp.test(e.target.value)) {
        this.conditions.lowercase = true;
      } else if (/\d/.test(e.target.value)) {
        this.conditions.number = true;
      } else if (specialSymbolsRegExp.test(e.target.value)) {
        this.conditions.special = true;
      } else if (e.target.value.length >= 8) {
        this.conditions.length = true;
      } else {
        return null;
      }
    },
  },
};
</script>

<style scoped>
.passwordWrapper {
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
#conditions {
  display: flex;
  justify-content: space-between;
  align-items: start;
  flex-flow: row wrap;
  list-style: none;
  width: 80%;
  margin-left: 1rem;
}
li {
  flex-basis: 50%;
  font-size: 12px;
  word-wrap: break-word;
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
  background-color: rgb(101, 196, 101);
  display: block;
  width: 100%;
  margin-top: 1rem;
  height: 0.5rem;
}
@media screen and (min-width: 800px) {
  #formWrapper {
    height: 70%;
    width: 40%;
    border: 5px solid black;
  }
}
@media screen and (min-width: 1200px) {
  #conditions {
    margin-top: 0.5rem;
  }
  input {
    width: 70%;
  }
}
</style>
