<template>
  <div class="w-full px-10 mx-auto">
    <div class="h-screen flex justify-center items-center">
      <!-- Form Container -->
      <div class="flex form-container rounded shadow-lg">
        <!-- Your Order Container -->
        <div class="flex-1 custom-bg">
          <img src="#" alt="">
          <h4>Your Order</h4>
          <div>
            <img src="#" alt="">
          </div>
          <ul>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
          </ul>
          <h4>Total</h4>
          <h4>$145.98</h4>
        </div>
        <!-- Pay Container -->
        <div class="flex-1 p-10 grid gap-y-8">
          <h4 class="uppercase">Pay with Credit Card</h4>
          <input type="text">
          <input type="text">
          <div>
            <select name="" id=""></select>
            <select name="" id=""></select>
            <input type="number" name="" id="">
          </div>
          <input type="submit" value="PAY SECURELY">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  .custom-bg {
    background-color: #f7eee9;
  }
</style>
