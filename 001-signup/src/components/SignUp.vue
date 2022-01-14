<template>
  <form class="grid gap-y-8" action="">
    <input class="custom-input name-input" type="text" name="name" id="name" placeholder="Name">
    <input class="custom-input email-input" type="email" name="email" id="email" placeholder="Email">
    <input class="custom-input password-input" type="password" name="password" id="password" placeholder="Password">
    <div class="flex justify-evenly px-4">
      <div class="custom-checkbox">
        <input type="radio" class="mr-2" id="male" name="gender" value="M">
        <label for="male">Male</label>
      </div>
      <div class="custom-checkbox">
        <input type="radio" class="mr-2" id="female" name="gender" value="F" checked>
        <label for="female">Female</label>
      </div>
    </div>
    <button class="btn-main py-4">SIGN UP</button>
    <span class="divider">or</span>
    <button class="btn-alternate py-4">Sign Up with Facebook</button>
  </form>
</template>

<script>
export default {
  name: 'SignUp_Form'
}
</script>

<style scoped>
  .name-input {
    background-image: url('../assets/user.svg');
  }

  .email-input {
    background-image: url('../assets/email.svg');
  }

  .password-input {
    background-image: url('../assets/pass.svg');
  }

  .custom-checkbox {
    font-size: 14px;
  }

  .custom-checkbox input[type=radio] { 
    display: none;
  }
</style>