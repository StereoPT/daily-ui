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
    <button class="btn btn-login py-4">LOG IN</button>
    <span class="divider">or</span>
    <button class="btn btn-login-facebook py-4">
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

  .custom-checkbox { 
    font-size: 12px;
  }

  .custom-checkbox label { 
    display: inline-block;
  }

  #remember { 
    display: none;
  }

  .custom-checkbox label:before {
    content: '';

    cursor: pointer;
    vertical-align: middle;
    color: black;

    line-height: 1.1em;
    font-weight: bold;
    text-align: center;
    font-size: 9px;
    height: 12px;
    width: 12px;
    margin-right: 0.25rem;
    display: inline-block;
    border: 1px solid #57ffff;
    box-sizing: border-box;
  }

  :checked+label:before {
    content: '\2713';
    color: #57ffff;
  }

  .custom-checkbox input {
    background-color: transparent;
  }

  .custom-link {
    font-size: 12px;
    text-decoration: underline;
    cursor: pointer;
  }

  .btn-login {
    font-size: 16px;
    font-weight: 800;
    background-color: #fca842;
    margin: 0 1rem 0 1rem;
  }

  .divider::before,
  .divider::after {
      display: inline-block;
      content: "";
      vertical-align: middle;
      border-top: 1px solid #57ffff;
      width: 2.5rem;
      margin: 0 0.75rem;
  }

  .btn-login-facebook {
    font-size: 16px;
    background-image: url('../assets/f.svg');
    background-color: #2e78be;
    background-size: 16px;
    background-position: left 1.5rem center;
    background-repeat: no-repeat;
    margin: 0 1rem 0 1rem;
    padding-left: 1.5rem;
  }
</style>