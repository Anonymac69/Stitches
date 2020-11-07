<template>
  <footer id="contact">
    <showbox/>

    <div class="info">
      <div class="info-brand">
        <p>Gstitches</p>
      </div>
      <div class="info-links">
          <nuxt-link class="li" to="#about">About</nuxt-link>
          <nuxt-link class="li" to="#packages">Packages</nuxt-link>
          <nuxt-link class="li" to="#contact">Contact</nuxt-link>
      </div>
      <div class="info-social">
          <a class="icon" href="twitter.com/gstitches"><span uk-icon="twitter"></span></a>
          <a class="icon" href="instagram.com/gstitches"><span uk-icon="instagram"></span></a>
          <a class="icon" href="facebook.com/gstitches"><span uk-icon="facebook"></span></a>
      </div>
    </div>

    <small class="copyright">&copy; Copyright Anonymac. 2020</small>
  </footer>
</template>

<script>
export default {

}
</script>

<style>
/* font-family: 'Pacifico', cursive; */
/* font-family: 'Poppins', sans-serif; */

footer {
  align-items: center;
  background: #f6f8fa;
  color: #8a8a8a;
  display: flex;
  flex-direction: column;
  font-family: 'Poppins', sans-serif;
  display: flex;
  justify-content: center;
  width: 100%;
}

.copyright {
  color: #959da5;
  font-family: 'Poppins', sans-serif;
  font-size: 11px;
  margin: 10px auto;
}

.info {
  align-items: center;
  border-top: 1px solid #e0e0e0;
  display: flex;
  justify-content: space-between;
  margin: 0 0 10px 0;
  padding: 20px;
  width: 90%;
}

.info-brand {
  align-items: center;
  display: flex;
  flex: 1 1 30%;
  justify-content: center;
  height: 50px;
}

.info-brand p {
  color: #24292e;
  font-family: 'Pacifico', cursive;
  font-size: 22px;
  margin: 0;
}

.info-links {
  align-items: center;
  display: flex;
  flex: 1 1 30%;
  height: 50px;
  justify-content: center;
}

.info-links .li {
  color: #24292e;
  font-size: 12px;
  margin: 10px;
  text-decoration: none;
}

.info-social {
  align-items: center;
  color: #24292e;
  display: flex;
  flex: 1 1 30%;
  height: 50px;
  justify-content: center;
}

.info-social .icon {
  color: #24292e;
  margin: 0 10px;
}

.info-social .icon-wrap {
  margin-left: 0 !important;
}

@media screen and (max-width: 800px) {
  .info-links {
    display: none;
  }
}


@media screen and (max-width: 480px) {
  .info-brand {
    display: none;
  }
}

</style>