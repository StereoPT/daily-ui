<template>
  <form action="">
    <input type="text" name="username" id="username">
    <br>
    <input type="password" name="password" id="password">
    <br>
    <input type="checkbox" id="remember" name="remember">
    <label for="remember"> Remember Me</label>
    <span>Forgot Password</span>
    <br>
    <button>LOG IN</button>
    <br>
    <span>or</span>
    <br>
    <button>Log In with Facebook</button>
  </form>
</template>

<script>
export default {
  name: 'SignIn_Form'
}
</script>