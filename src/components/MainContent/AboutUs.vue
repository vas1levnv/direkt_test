<template>
  <div class="aboutUs">
    <h2>
      О нас
    </h2>
    <div class="description">
      <p>Цент –– это агенство, представляющее полный
        комплекс услуг в области digital - маркетинга
        и креатива. Агентсво обладает крупнейшей
        инфраструктурой в социальных сетях
        в мире. </p>
      <div class="description-link">
        <a href="#">Связаться</a>
        <a href="#">Больше о нас</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutUs"
}
</script>

<style scoped>
.aboutUs {
  display: flex;
  padding: 80px 0 160px;
  justify-content: space-between;
}

h2 {
  display: block;
  min-width: 200px;
  font-weight: 700;
}

.description {
  max-width: 400px;
}

.description p {
  margin-bottom: 80px;
}

.description-link {
  display: flex;
  justify-content: space-between;
  font-weight: 700;
}
.description-link a{
  font-size: 16px;
}

@media (max-width: 768px) {
  .aboutUs {
    display: block;
    padding: 40px 0 80px;
  }

  h2 {
    margin-bottom: 20px;
  }

}

</style>