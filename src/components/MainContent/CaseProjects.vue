<template>
  <div class="caseProjects">
    <h2>Кейсы</h2>
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
  name: "CaseProjects",
  props: {
    posts: {
      type: Array,
      required: true,
    }
  },
}


</script>

<style scoped>

.caseProjects{
  max-height: 1300px;
  z-index: 3;
  overflow-y: auto;
}

h2{
  margin-bottom: 60px;
}

.posts {
  display: grid;
  grid-template-columns: repeat(2,minmax(200px, 600px));
  row-gap: 40px;
  column-gap: 50px;
}

.post img{
  width: 100%;
  object-fit: none;
}

h3{
  margin-top: 15px;
  font-size: 16px;
  font-weight: 700;
}

p{
  margin-top: 15px;
  font-size: 12px;
}

@media (max-width: 768px){

  .caseProjects{
    max-height: 700px;
  }

  h2{
    margin-bottom: 25px;
  }
  .posts {
    display: grid;
    grid-template-columns: repeat(1,minmax(200px, 600px));
    row-gap: 30px;
  }
  h3{
    margin-top: 0;
  }

  p{
    margin-top: 0;
  }
  .post img{
    width: 100%;
    object-fit: contain;
  }
}

</style>