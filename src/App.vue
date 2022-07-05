<template>
  <Header/>
  <MainContent :posts="posts"/>
  <OurAssets :ourAssets="ourAssets"/>
  <OurClients/>
  <Footer/>



</template>


<script>
import Header from "@/components/Header";
import MainContent from "@/components/MainContent/MainContent";
import OurAssets from "@/components/OurAssets";
import OurClients from "@/components/OurClients/OurClients";
import Footer from "@/components/Footer";

export default {
  components: {
    Header,
    MainContent,
    OurAssets,
    OurClients,
    Footer
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Итоги года 2021', description: 'Ежегодная премия', name: 'Rectangle 149.png'},
        {id: 2, title: 'Фестиваль «Профсоюзная»', description: 'Уличный фестиваль', name: 'Rectangle 151.png'},
        {id: 3, title: 'Enter x Водоканал', description: 'Рекламная коммуникация', name: 'Rectangle 150.png'},
        {id: 4, title: 'Мой прекрасный Татарстан', description: 'Фотомарафон', name: 'Rectangle 152.png'},
        {id: 5, title: 'Итоги года 2021', description: 'Ежегодная премия', name: 'Rectangle 145.png'},
        {id: 6, title: 'Фестиваль «Профсоюзная»', description: 'Уличный фестиваль', name: 'Rectangle 146.png'},
        {id: 7, title: 'Enter x Водоканал', description: 'Рекламная коммуникация', name: 'Rectangle 147.png'},
        {id: 8, title: 'Мой прекрасный Татарстан', description: 'Фотомарафон', name: 'Rectangle 2.png'},
      ],

      ourAssets: [
        {id: 1, name: 'Rectangle 167.png'},
        {id: 2, name: 'Rectangle 168.png'},
        {id: 3, name: 'Rectangle 1.png'},
        {id: 4, name: 'Rectangle 170.png'},
        {id: 5,name: 'Rectangle 147.png'},
        {id: 6, name: 'Rectangle 2.png'},
        {id: 7, name: 'Rectangle 173.png'},
        {id: 8, name: 'Rectangle 146.png'},
      ],
      /*posts: [
        {id: 1, title: 'Пост', body: 'язык програмирования'},
        {id: 2, title: 'Пост 2', body: 'язык програмирования 2'},
      ],*/
    }
  },
  methods: {
    /*createPost(post){
      this.posts.push(post)
    }*/
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Montserrat;
  font-size: 20px;

}
::-webkit-scrollbar {
  width: 0;
}
@font-face {
  font-family: "Montserrat";
  src: local("Montserrat"),
  url(./fonts/Montserrat-VariableFont_wght.ttf) format("truetype");
}

.container {
  max-width: 1180px;
  margin: 0 auto;
  padding: 0 15px;
}

a {
  color: #fff;
  text-decoration: none;
}

.app {
  padding: 20px;
}


h2{
  font-size: 30px;
}

@media (max-width: 768px) {
  *{
    font-size: 16px;
  }
  h2{
    font-size: 24px;
  }
}

</style>