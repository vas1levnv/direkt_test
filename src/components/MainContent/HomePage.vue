<template>
  <div class="home-page">
    <div class="container">
      <h1>Больше чем тенге</h1>
      <div class="info">
        <div class="address">
          Казань, Карла Маркса 5
        </div>
        <div class="mail">
          <a href="mailto:someone@example.com">info@cent</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomePage"
}

</script>

<style scoped>

.home-page {
  /*  background: url("../../img/Frame 45.png") no-repeat center;
    background-size: contain;*/
  position: relative;
  overflow: hidden;
}

.container {
  height: 80vh;
  display: grid;
}

h1 {
  display: block;
  text-align: center;
  align-self: end;
  padding-bottom: 40px;
  font-size: 82px;
  font-weight: 900;
}

.info {
  display: flex;
  justify-content: space-between;
  align-self: end;
  padding-bottom: 40px;
  position: relative;
}

.mail:after{
  content:url("~@/img/Vector.svg");
  display: block;
  position: absolute;
  transform: translateY(1000px);
  transition: transform .5s ease;
}

.mail:hover:after{
  transform: translateX(-13px) translateY(-120px);
}



@media (max-width: 768px) {
  h1 {
    font-size: 42px;
  }
.address{
  width: 150px;
}

  .info {
    font-size: 16px;
  }

  .mail:after{
    display: none;
  }

}

</style>