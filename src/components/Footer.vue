<template>
  <div class="footer">
    <div class="container">
      <div class="description">
        <h2>Контакты</h2>
        <div class="address">
          <p>8 800 700 60 50</p>
          <p>info@cent</p>
          <p>Казань, Карла Маркса 9</p>
        </div>
        <div class="company">
          <p>Агенство Cent, 2017</p>
        </div>
      </div>
      <div class="fieldInput">
        <input type="text" placeholder="Ваше имя">
        <input type="text" placeholder="Email">
        <input type="text" placeholder="Телефон">
        <input type="text" placeholder="Что вы ищете">
        <input type="text" placeholder="Сообщение">
      </div>
    </div>
    <div class="container-mobile">
      <div class="description">
        <h2>Контакты</h2>
        <div class="fieldInput">
          <input type="text" placeholder="Ваше имя">
          <input type="text" placeholder="Email">
          <input type="text" placeholder="Телефон">
          <input type="text" placeholder="Что вы ищете">
          <input type="text" placeholder="Сообщение">
        </div>
        <div class="address">
          <p>8 800 700 60 50</p>
          <p>info@cent</p>
          <p>Казань, Карла Маркса 9</p>
        </div>
        <div class="company">
          <p>Агенство Cent, 2017</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>
.footer {
  background: #001CAD;
  color: white;
  padding: 80px 0 100px;
}

.container {
  display: flex;
  justify-content: space-between;
}

.container-mobile {
  display: none;
}

.address {
  margin-top: 70px;
}

.company {
  margin-top: 70px;
}

.fieldInput {
  align-self: flex-start;
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 14px;
  row-gap: 9px;

}

input {
  background: #0024DC;
  box-sizing: border-box;
  border: none;
  padding: 0 0 0 10px;
  height: 47px;
  width: 242px;
  font-size: 12px;
}

input:last-child {
  grid-column: 1/3;
  width: 100%;
  height: 171px;
}

input:last-child::placeholder {
}

input::placeholder {
  color: white;
}


@media (max-width: 768px) {
  .footer {
    padding: 45px 0 45px;
  }

  .container{
    display: none;
  }

  h2{
    text-align: start;
    margin-bottom: 25px;
  }

.container-mobile{
  text-align: center;
 padding: 0 15px;
  display: flex;
  justify-content: center;
}
  .fieldInput {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
}

</style>