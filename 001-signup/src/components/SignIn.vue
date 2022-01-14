<template>
  <form class="grid gap-y-8" action="">
    <input class="custom-input user-input" type="text" name="username" id="username" placeholder="Username">
    <input class="custom-input password-input" type="password" name="password" id="password" placeholder="Password">
    <div class="flex justify-between px-2">
      <div>
        <input type="checkbox" id="remember" name="remember">
        <label for="remember"> Remember Me</label>
      </div>
      <span>Forgot Password</span>
    </div>
    <button class="btn-login py-4">LOG IN</button>
    <span>or</span>
    <button class="btn-login-facebook py-4">Log In with Facebook</button>
  </form>
</template>

<script>
export default {
  name: 'SignIn_Form'
}
</script>

<style scoped>
  .custom-input {
    font-size: 14px;
    border-bottom: 1px solid #57ffff;
    padding: 0.5rem;
    background-color: transparent;
    background-size: 16px;
    background-position: right 0.5rem center;
    background-repeat: no-repeat;
    padding-right: 2rem;
  }

  .user-input {
    background-image: url('../assets/user.svg');
  }

  .password-input {
    background-image: url('../assets/pass.svg');
  }

  .custom-input:focus {
    outline: none;
  }

  .btn-login {
    background-color: #fca842;
  }

  .btn-login-facebook {
    background-color: #2e78be;
  }
</style>