<template>
  <div class="w-full px-10 mx-auto">
    <div class="h-screen flex justify-center items-center">
      <!-- Form Container -->
      <div class="form-container">
        <!-- Form Tabs -->
        <div class="flex text-center">
          <div
            class="flex-1 py-4 cursor-pointer"
            :class="signInTab ? 'active-tab' : 'bg-white'"
            @click="toggleTab('signin')">
            <a>Sign In</a>
          </div>
          <div
            class="flex-1 py-4 cursor-pointer"
            :class="signInTab ? 'bg-white' : 'active-tab'"
            @click="toggleTab('signup')">
            <a>Sign Up</a>
          </div>
        </div>
        <!-- Form Content -->
        <div class="text-center py-10">
          <div v-if="signInTab">
            <!-- Sign In Form -->
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
          </div>
          <div v-else>
            <!-- Sign Up Form -->
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
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '001-SignUp',
  data() {
    return {
      signInTab: true
    }
  },
  methods: {
    toggleTab(btn) {
      if(btn === 'signin') this.signInTab = true;
      else if(btn === 'signup') this.signInTab = false;
    }
  }
}
</script>

<style>
  body {
    background-color: #dedede;
  }

  .form-container {
    min-width: 480px;
    background-color: #23383E;
  }

  .active-tab {
    background-color: #23383E;
  }
</style>
