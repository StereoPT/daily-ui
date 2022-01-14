<template>
  <div class="w-full px-10 mx-auto">
    <div class="h-screen flex justify-center items-center">
      <!-- Form Container -->
      <div class="form-container">
        <!-- Form Tabs -->
        <div class="flex text-center">
          <div
            class="flex-1 py-4 cursor-pointer tab"
            :class="signInTab ? 'active-tab' : 'inactive-tab'"
            @click="toggleTab('signin')">
            <a>Sign In</a>
          </div>
          <div
            class="flex-1 py-4 cursor-pointer tab"
            :class="signInTab ? 'inactive-tab' : 'active-tab'"
            @click="toggleTab('signup')">
            <a>Sign Up</a>
          </div>
        </div>
        <!-- Form Content -->
        <div class="text-center text-white p-14">
          <SignIn v-if="signInTab" />
          <SignUp v-else />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SignIn from './components/SignIn.vue';
import SignUp from './components/SignUp.vue';

export default {
  name: '001-SignUp',
  components: {
    SignIn, SignUp
  },
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
    background: url('./assets/background.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }

  .form-container {
    min-width: 380px;
    min-height: 640px;
    background-color: rgba(35, 56, 62, 0.85);
  }

  .tab a {
    font-weight: 600;
  }

  .active-tab {
    color: white;
  }

  .inactive-tab {
    background-color: white;
    color: #4ad9d9;
  }
</style>
