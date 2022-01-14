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

  .custom-input:focus {
    outline: none;
  }

  .custom-checkbox label { 
    display: inline-block;
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

  .btn-main {
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

  .btn-alternate {
    font-size: 16px;
    background-image: url('./assets/f.svg');
    background-color: #2e78be;
    background-size: 16px;
    background-position: left 1.5rem center;
    background-repeat: no-repeat;
    margin: 0 1rem 0 1rem;
    padding-left: 1.5rem;
  }
</style>
