<template>
  <div class="w-full px-10 mx-auto">
    <div class="h-screen flex justify-center items-center">
      <!-- Form Container -->
      <div class="form-container bg-red-500">
        <div class="flex text-center">
          <!-- Form Tabs -->
          <div class="flex-1 py-4 bg-gray-300 cursor-pointer" @click="toggleTab('signin')">
            <a>Sign In</a>
          </div>
          <div class="flex-1 py-4 bg-gray-300 cursor-pointer" @click="toggleTab('signup')">
            <a>Sign Up</a>
          </div>
        </div>
        <div class="text-center py-10" v-if="signInTab">
          <!-- Sign In Form -->
          <h1 class="text-3xl font-bold underline">
            Sign In
          </h1>
        </div>
        <div class="text-center py-10" v-else>
          <!-- Sign Up Form -->
          <h1 class="text-3xl font-bold underline">
            Sign Up
          </h1>
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
  }
</style>
