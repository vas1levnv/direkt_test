<template>
  <div class="home-page">
    <h1>Больше чем тенге</h1>
    <div class="info">
      <div class="address">
        Казань, Карла Маркса 5
      </div>
      <div class="mail">
        info@cent
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
.home-page{
  height:80vh;
display: grid;
}
h1{
  display: block;
  text-align: center;
  align-self: end;
  padding-bottom: 40px;
  font-size: 82px;
  font-weight: 900;
}

.info{
  display: flex;
  justify-content: space-between;
  align-self: end;
  padding-bottom: 40px;
}

@media (max-width: 768px){
  h1{
    font-size: 42px;
  }

  .info{
    font-size: 16px;
  }

}

</style>