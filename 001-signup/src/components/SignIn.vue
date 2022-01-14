<template>
  <form class="grid gap-y-8">
    <input class="custom-input user-input" type="text" name="username" id="username" placeholder="Username">
    <input class="custom-input password-input" type="password" name="password" id="password" placeholder="Password">
    <div class="flex justify-between px-2">
      <div class="custom-checkbox">
        <input type="checkbox" id="remember" name="remember">
        <label for="remember">Remember me</label>
      </div>
      <a class="custom-link">Forgot password</a>
    </div>
    <button class="btn-main py-4">LOG IN</button>
    <span class="divider">or</span>
    <button class="btn-alternate py-4">
      Log In with Facebook
    </button>
  </form>
</template>

<script>
export default {
  name: 'SignIn_Form'
}
</script>

<style scoped>
  .user-input {
    background-image: url('../assets/user.svg');
  }

  .password-input {
    background-image: url('../assets/pass.svg');
  }

  .custom-checkbox { 
    font-size: 12px;
  }

  #remember { 
    display: none;
  }

  .custom-link {
    font-size: 12px;
    text-decoration: underline;
    cursor: pointer;
  }
</style>