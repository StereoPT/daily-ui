<template>
  <form class="grid gap-y-8" action="">
    <input class="bg-transparent py-1 px-2" type="text" name="name" id="name" placeholder="Name">
    <input class="bg-transparent py-1 px-2" type="email" name="email" id="email" placeholder="Email">
    <input class="bg-transparent py-1 px-2" type="password" name="password" id="password" placeholder="Password">
    <div class="flex justify-evenly px-4">
      <div>
        <input type="radio" class="mr-2" id="male" name="gender" value="M">
        <label for="male">Male</label>
      </div>
      <div>
        <input type="radio" class="mr-2" id="female" name="gender" value="F" checked>
        <label for="female">Female</label>
      </div>
    </div>
    <button class="btn-signup py-4">SIGN UP</button>
    <span>or</span>
    <button class="btn-signup-facebook py-4">Sign Up with Facebook</button>
  </form>
</template>

<script>
export default {
  name: 'SignUp_Form'
}
</script>

<style scoped>
  .btn-signup {
    background-color: #fca842;
  }

  .btn-signup-facebook {
    background-color: #2e78be;
  }
</style>