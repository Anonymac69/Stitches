<template>
  <main class="container">
    <navigation/>
    <form class='log-wrap' action="">
    <h3 class="log-title">Create an Account</h3>
      <div class="">
        <label for="username"></label>
        <input class="log-value" type="text" placeholder="Username">
      </div>
      <div class="">
        <label for="email"></label>
        <input class="log-value" type="email" placeholder="email">
      </div>
      <div class="">
        <label for="password"></label>
        <input class="log-value" name="password" placeholder="password">
      </div>
      <div class="">
        <button class="log-submit" type="submit" name="password" id="email">Login</button>
      </div>
      <div class="log-error">
        <small><a class="log-error-pssw" href="#">Forgot Password?</a></small>
        <nuxt-link class="log-error-signup" to="/auth/login"><small>Login</small></nuxt-link>
      </div>

    </form>
  </main>
</template>

<script>
export default {

}
</script>

<style>

</style>