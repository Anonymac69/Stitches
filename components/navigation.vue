<template>
  <nav class="nav-box" :class="{ 'nav--hidden': !showNavbar }">
    <h2><nuxt-link class="nav-brand" to="/">Gstitches</nuxt-link></h2>
    <ul class="nav-links">
      <nuxt-link class="li" to="#about">About</nuxt-link>
      <nuxt-link class="li" to="#packages">Packages</nuxt-link>
      <nuxt-link class="li" to="#contact">Contact</nuxt-link>
    </ul>
    
    <span class="nav-menu" uk-icon="icon: menu; ratio: 1.2" uk-toggle="target: #offcanvas-slide"></span>
    <div id="offcanvas-slide" uk-offcanvas="overlay: true; flip: true">
        <div class="uk-offcanvas-bar">        
            <button class="uk-offcanvas-close" type="button" uk-close></button>                
            <ul class="nav-menu-links">
                <nuxt-link class="li" to="#about">About</nuxt-link>
                <nuxt-link class="li" to="#packages">Packages</nuxt-link>
                <nuxt-link class="li" to="#contact">Contact</nuxt-link>
            </ul>        
        </div>
    </div>

  </nav>
</template>

<script>
export default {
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0
    }
  },
  mounted() {
    window.addEventListener('scroll', this.onScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.onScroll)
  },
  methods: {
    onScroll () {
      // Get the current scroll position
      const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop    
      // Because of momentum scrolling on mobiles, we shouldn't continue if it is less than zero
      if (currentScrollPosition < 0) {
        return
      }
      // Stop executing this function if the difference between
      // current scroll position and last scroll position is less than some offset

      if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 60) {
        return
      }
      this.showNavbar = currentScrollPosition < this.lastScrollPosition
      // Set the current scroll position as the last scroll position
      this.lastScrollPosition = currentScrollPosition
    }
  }}
</script>

<style>
/* font-family: 'Pacifico', cursive; */
/* font-family: 'Poppins', sans-serif; */

nav {
  align-items: baseline;
  background: #f6f8fa;
  display: flex;
  justify-content: space-between;
  padding: 0 20px;
  position: fixed;
  transform: translate3d(0, 0, 0);
  transition: 0.1s all ease-out;
  width: 100%;
}

.nav-brand, 
.nav-brand:hover {
  color: #24292e;
  font-family: 'Pacifico', cursive;
  font-size: 24px;
  text-decoration: none;
}

nav.nav--hidden {
  transform: translate3d(0, -100%, 0)
}

.nav-links {
  display: flex;
}

.nav-links .li {
  color: #24292e;
  font-family: 'Poppins', sans-serif;
  font-size: 12px;
  list-style: none;
  margin: 0 25px 0 0;
  text-decoration: none;
  transition: color 0.5s;
}

.nav-links .li:hover {
  color: #c108ff;
  font-family: 'Poppins', sans-serif;
  font-size: 12px;
  list-style: none;
  margin: 0 25px 0 0;
  text-decoration: none;
}

.nav-menu-links {
  display: flex;
  flex-direction: column;
  list-style: none;
  margin: 50px 0;
  text-decoration: none;
}

.nav-menu-links .li {
  color: #fff;
  font-family: 'Poppins', sans-serif;
  font-size: 16px;
  font-weight: 500;
  margin: 20px 0;
  text-decoration: none;
}

.nav-menu {
  color: #24292e;
  display: none;
}

@media screen and (max-width: 1000px) {
  .nav-links {
    display: none;
  }
  .nav-menu {
    display: inline;
    margin: 20px 0;
  }
}



</style>