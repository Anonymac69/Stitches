<template>
  <main class='panel-wrap'>
    <p class="panel-title">Showcase</p>
    <hr class="line-alt">

    <section class="panel">
      <div class="pane p01">
        <section class="pane-mssg-box"  uk-scrollspy="cls: uk-animation-slide-left; repeat: true">
          <small>{{message}}</small>
        </section>
      </div>

      <div class="pane p02">
        <section class="pane-mssg-box"  uk-scrollspy="cls: uk-animation-slide-bottom; repeat: true">
          <small>{{message}}</small>
        </section>
      </div>

      <div class="pane p03">
        <section class="pane-mssg-box"  uk-scrollspy="cls: uk-animation-slide-right; repeat: true">
          <small>{{message}}</small>
        </section>
      </div>
    </section>

  </main>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello World'
    }
  },
}
</script>

<style>
/* font-family: 'Pacifico', cursive; */
/* font-family: 'Poppins', sans-serif; */

.p01 {
  background: url('https://images.unsplash.com/photo-1552710307-537199cd41c0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=400&q=60');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.p02 {
  background: url("https://images.unsplash.com/photo-1538330627166-33d1908c210d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=400&q=60");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.p03 {
  background: url('https://images.pexels.com/photos/871494/pexels-photo-871494.jpeg?auto=compress&cs=tinysrgb&dpr=3&h=750&w=1260');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.pane {
  align-items: flex-end;
  display: flex;
  flex: 1 1 30%;
  height: 100%;
  justify-content: flex-end;
}

.pane-mssg-box {
  align-items: center;
  background: #000;
  border-radius: .2rem;
  display: flex;
  height: 100px;
  justify-content: center;
  margin: 10px;
  width: 50%;
}

.panel {
  background: #f6f8fa;
  display: flex;
  height: 300px;
  margin: 50px auto;
  width: 100%;
}

.panel-title {
  color: #24292e;
  font-family: 'Poppins', sans-serif;
  margin: 20px 0 0 0;
  font-size: 35px;
}

.panel-wrap {
  align-items: center;
  /* border: 1px solid #ff65a0; */
  display: flex;
  flex-direction: column;
  margin: 30px auto;
  height: 100%;
  width: 100%;
}

@media screen and (max-width: 800px) {
  .panel {
    flex-direction: column;
    height: 1000px;
  }
}
</style>