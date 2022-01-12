<template>
  <form action="">
    <input type="text" name="name" id="name">
    <br>
    <input type="text" name="username" id="username">
    <br>
    <input type="password" name="password" id="password">
    <br>
    <input type="radio" id="male" name="gender" value="M">
    <label for="male">Male</label>
    <input type="radio" id="female" name="gender" value="F" checked>
    <label for="female">Female</label>
    <br>
    <button>SIGN UP</button>
    <br>
    <span>or</span>
    <br>
    <button>Sign Up with Facebook</button>
  </form>
</template>

<script>
export default {
  name: 'SignUp_Form'
}
</script>