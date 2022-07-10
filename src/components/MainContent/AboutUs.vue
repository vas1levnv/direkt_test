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
        <a @mouseover="show = true" @mouseleave="show = false" class="hover-link" >Больше о нас</a>
      </div>
    </div>
  </div>
  <transition name="fade">
    <div v-if="show" class="aboutUs-more">
    <div class="mass-media">
      <p class="title">СМИ</p>
      <p class="numbers">> 2 МЛН</p>
      <p class="text">ЕЖЕМЕСЕЧНАЯ АУДИТОРИЯ</p>
    </div>
    <div class="social-media">
      <p class="title">СОЦСЕТИИ</p>
      <p class="numbers">> 14 МЛН</p>
      <p class="text">ЕЖЕМЕСЕЧНЫЙ ОХВАТ</p>
    </div>
    <div class="pr">
      <p class="title">PR</p>
      <p class="numbers">> 30</p>
      <p class="text">РЕШЕННЫХ ИНФОРМАЦИОННЫХ КРИЗИСОВ</p>
    </div>
    <div class="creative">
      <p class="title">КРЕАТИВ</p>
      <p class="numbers">> 150</p>
      <p class="text-bottom">ИНФОПОВОДОВ<br>ФЕДЕРАЛЬНОГО УРОВНЯ</p>
    </div>
    <div class="blogers">
      <p class="title">БЛОГЕРЫ</p>
      <p class="numbers">> 1000</p>
      <p class="text-bottom">ИНТЕГРАЦИИ<br>С ИНФЛЮЕНСЕРАМИ </p>
    </div>
    <div class="evetns">
      <p class="title">МЕРОПРИЯТИЯ</p>
      <p class="numbers">> 400</p>
      <p class="text-bottom">СОБЫТИЙ РЕГИОНАЛЬНОГО<br>И ФЕДЕРАЛЬНОГО МАСШТАБА<br>С ОБЩИМ ОХВАТОМ 45 МЛН</p>
    </div>
  </div>
  </transition>

</template>

<script>
export default {
  data() {
    return {
      show: false
    }
  },

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
  justify-content: flex-start;
  font-weight: 700;
}


.description-link a {
  font-size: 16px;
}

.hover-link{
padding-left: 55px;
}
transition{

}

.aboutUs-more {
  font-size: 38px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 100px;
  padding: 0 0 150px 0;
  position: absolute;
  background: #0E0E0E;
  transition: all 0.5s ease-out;
}

.mass-media, .social-media, .creative, .blogers {
  border-right: 1px #BFBFBF solid;
}

.title {
  color: #BFBFBF;
  font-size: 38px;
  font-weight: 900;
  margin-bottom: 60px;
}

.numbers {
  font-size: 38px;
  font-weight: 900;
}

.text {
  font-size: 12px;
  margin-bottom: 160px;
}

.text-bottom {
  font-size: 12px;
  margin: 0;
}

@media (max-width: 1200px) {
  .aboutUs-more{
    column-gap: 50px;
  }
.title, .numbers{
  font-size: 24px;
}
}

@media (max-width: 768px) {
  .aboutUs {
    display: block;
    padding: 40px 0 80px;

  }

  h2 {
    margin-bottom: 20px;
  }

  .aboutUs-more{
    grid-template-columns: repeat(2, 1fr);
    gap: 0;
  }

  .title {
    color: #BFBFBF;
    font-size: 24px;
    font-weight: 900;
    margin-top: 50px;
  }

  .description-link{
    justify-content: space-between;
  }

  .mass-media, .social-media, .creative, .blogers {
    border-right: 0;
  }

  .mass-media, .social-media, .creative, .pr {
    border-bottom: 1px #BFBFBF solid;
  }

  .blogers, .evetns{
    grid-column-start: 1;
    grid-column-end: 3;
    text-align: center;
  }

  .text-bottom, .text {
    font-size: 10px;
    margin-bottom: 50px;
    padding-right: 10px;
  }
  .hover-link{
    padding-left: 0;
  }
}

</style>