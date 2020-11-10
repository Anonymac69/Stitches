<template>
  <main class="container">
    <navigation/>
    <form class='log-wrap' action="" v-if="!newUser">
    <h3 class="log-title">Login</h3>
      <div class="">
        <label for="email"></label>
        <input class="log-value" placeholder="johndoe@example.com" type="email" id="email">
      </div>
      <div class="">
        <label for="password"></label>
        <input class="log-value" placeholder="password" name="password" id="password">
      </div>
      <div class="">
        <button class="log-submit" type="submit" name="password" id="email">Login</button>
      </div>
      <div class="log-error">
        <small><a class="log-error-pssw" href="">Forgot Password?</a></small>
        <nuxt-link class="log-error-signup" to="/auth/signup"><small>Sign Up</small></nuxt-link>
      </div>
    </form>
  </main>
</template>

<script>
export default {
  data() {
    return {
      newUser: false,
    }
  },
  methods: {
    createUser() {
      this.newUser = true
    }
  }
}
</script>

<style>
  .log-error {
    align-items: center;
    color: #fff;
    display: flex;
    justify-content: space-between;
    padding: 0 5px;
    width: 22rem;
  }

  .log-error-pssw,
  .log-error-pssw:hover {
    color: #fff;
    text-decoration: none;
  }

  .log-error-signup,
  .log-error-signup:hover {
    color: #fff;
    text-decoration: none;
  }

  .log-submit {
    background: #c108ff;
    border: none;
    border-radius: .2rem;
    color: #fff;
    font-family: 'Poppins', sans-serif;
    font-size: 1rem;
    font-weight: 100;
    height: 2.8rem;
    margin: .5rem;
    outline: none;
    width: 22rem;

  }

  .log-title {
    color: #fff;
    font-family: 'Poppins', sans-serif;
    font-size: 2rem;
  }

  .log-value {
    background: #fff;
    border: none;
    border-radius: .2rem;
    color: #212121;
    font-family: 'Poppins', sans-serif;
    font-weight: 300;
    height: 2.8rem;
    margin: .5rem;
    padding: 10px;
    outline: none;
    width: 22rem;
  }

  .log-wrap {
    align-items: center;
    background: rgba(0, 0, 0, 0.8);
    /* border: 1px solid #ff4500; */
    display: flex;
    flex-flow: column wrap;
    height: 100vh;
    justify-content: center;
    margin: 0 auto;
    width: 100% !important;
  }
</style>