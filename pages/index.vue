<template>
  <div class="home-page">
    <section class="intro">
      <h1>工程師之路</h1>
    </section>
    <Swiper />
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "../components/Posts/PostList";
import Swiper from "../components/Swiper/Swiper";

export default {
  components: {
    PostList,
    Swiper,
  },
  async asyncData(context) {
    return await new Promise((resolve, reject) =>
      setTimeout(
        () =>
          resolve({
            loadedPosts: [
              {
                id: "1",
                thumbnail:
                  "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU",
                title: "第一篇文章",
                previewText: "這條路真的不好走....",
              },
              {
                id: "2",
                thumbnail:
                  "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU",
                title: "第二篇文章",
                previewText: "這條路真的不好走....",
              },
              {
                id: "3",
                thumbnail:
                  "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU",
                title: "第三篇文章",
                previewText: "這條路真的不好走....",
              },
              {
                id: "4",
                thumbnail:
                  "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU",
                title: "第四篇文章",
                previewText: "這條路真的不好走....",
              },
            ],
          }),
        1000
      )
    );
  },
};
</script>

<style scoped>
.home-page {
  height: 100px;
  width: 100%;
}
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url("../assets/images/1_18D2nMBUOE70LvsSRPiWBw.png");
  background-position: center;
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}
</style>
