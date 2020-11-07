<template>
  <main class="brand">
    <div class="brand-wrap">
      <p class="brand-title">Beyond the Fashion Statement</p>
      <hr class="line">
      <small class="brand-text">Gstitches is a progressive Fashion Design outfit birthed in 2020.</small>
    </div>
  </main>
</template>

<script>
export default {

}
</script>

<style>
.brand {
  align-items: center;
  display: flex;
  justify-content: flex-end;
  height: 100vh;
  padding: 0 50px;
  width: 90%;
}

.brand-text {
  color: #fff;
  font-family: 'Poppins', sans-serif;
  font-size: 12px;
  font-weight: 300;
}

.brand-title {
  color: #f6f8fa;
  font-family: 'Poppins', sans-serif;
  font-size: 35px;
  margin: 0;
}

.brand-wrap {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.line {
  background: #fff;
  height: 3px;
  margin: 20px 0;
  width: 70px;
}

.line-alt {
  background: #24292e;
  height: 3px;
  margin: 20px 0;
  width: 70px;
}

@media screen and (max-width: 800px) {
  .brand-wrap {
    align-items: center;
  }
}

</style>