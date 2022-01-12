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
            <SignIn />
          </div>
          <div v-else>
            <!-- Sign Up Form -->
            <SignUp />
          </div>
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
