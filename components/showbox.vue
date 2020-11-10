<template>
  <main class='panel-wrap'>
    <p class="panel-title">Showcase</p>
    <hr class="line-alt">

    <section class="panel">
      <div class="pane p01">
        <section class="pane-mssg-box"  uk-scrollspy="cls: uk-animation-slide-left; repeat: true">
          <div class="pane-mssg-box-title"> {{message}} </div>
          <small class="pane-mssg-box-text"> {{message}} </small>
        </section>
      </div>

      <div class="pane p02">
        <section class="pane-mssg-box"  uk-scrollspy="cls: uk-animation-slide-left; repeat: true">
          <div class="pane-mssg-box-title"> {{message}} </div>
          <small>{{message}}</small>
        </section>
      </div>

      <div class="pane p03">
        <section class="pane-mssg-box"  uk-scrollspy="cls: uk-animation-slide-left; repeat: true">
          <div class="pane-mssg-box-title"> {{message}} </div>
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
  background: rgba(0, 0, 0, 0.7);
  border-radius: .2rem;
  color: #fff;
  display: flex;
  flex-flow: column wrap;
  height: 70px;
  justify-content: space-between;
  margin: 10px;
  width: 50%;
}

.pane-mssg-box-title {
  background: #070707;
  width: 100%;
}

.panel {
  background: #f6f8fa;
  display: flex;
  height: 400px;
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