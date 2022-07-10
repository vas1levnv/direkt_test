<template>
  <div class="posts-content">
    <div class="posts-content__description">
      <div class="text">
        <h2>Итоги пиццы</h2>
        <p>Ежегодная премия</p>
        <p>Если экстраполировать культуру пиццы на Казань, то можно смело сказать, что казанцы «отменили» Баумана. Ее
          любят туристы и обходят местные, и такое положение давно пора менять. Перемены с целью вернуть главную
          пешеходную улицу горожанам уже начались, и пока они только на самом старте.</p>
        <p>
          24 мая в рамках дискуссионно-образовательной программы «Городские модераторы» редакция Enter совместно с
          мэрией Казани собрала желающих на первой дискуссии о том, какой должна стать улица Баумана в результате
          переустройства. Коротко пересказываем, о чем говорили участники и к чему они пришли.</p>
      </div>
      <img :src="postImg">
    </div>
    <div class="text-bottom">
      <p>Основная задача властей — поработать над улицей так, чтобы сделать ее привлекательной для разных клиентских
        групп. Для кого должна быть улица — вопрос открытый. Участники дискуссии из зала предложили отказаться от
        обозначений «туристам» и «жителем» и определить более точные критерии с помощью грамотного продуктолога; по их
        мнению, когда мы поймем, кому принадлежит Баумана, тогда и узнаем, какую ценность она в себе несет. Спикер и
        совладелец бара Kommunalka Андрей Блинов предложил сохранить Баумана универсальной, ведь уже сейчас в разное
        время она работает на разный сегмент граждан.</p>
    </div>
    <h3 style="text-align: center; margin: 0 0 40px 0">Другие кейсы</h3>
    <div class="posts">
      <div class="post" v-for="post in posts">
        <div><img :src="require(`../../img/${post.name}`)"></div>
        <h3>{{ post.title }}</h3>
        <p>{{ post.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PostsContent"
}
</script>

<style scoped>
h2 {
  margin-bottom: 60px;
}

.posts {
  display: grid;
  grid-template-columns: repeat(2, minmax(200px, 600px));
  row-gap: 40px;
  column-gap: 50px;
}

.post img {
  width: 100%;
  object-fit: none;
}

h3 {
  margin-top: 15px;
  font-size: 16px;
  font-weight: 700;
}

p {
  margin-top: 15px;
  font-size: 12px;
}

.posts-content__description {
  display: flex;
  justify-content: space-between;
  margin-top: 145px;
}

.posts-content{
  position: absolute;
  top: 0;
  left: 0;
  background: #0E0E0E;
  z-index: 20;
  transition: top 0.3s ease 0s;
}

.posts-content__description h2{
  margin: 0;
}
.posts-content__description img{
  width: 50%;
  object-fit: contain;
}
.text{
  padding-right: 55px;
}

.text-bottom{
  padding: 70px 0 60px;
}

@media (max-width: 768px) {

  h2 {
    margin-bottom: 25px;
  }

  .posts {
    display: grid;
    grid-template-columns: repeat(1, minmax(200px, 600px));
    row-gap: 30px;
  }

  h3 {
    margin-top: 0;
  }

  p {
    margin-top: 0;
  }

  .post img {
    width: 100%;
    object-fit: contain;
  }
}

</style>