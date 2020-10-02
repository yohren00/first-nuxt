<template>
  <div class="single-post-page">
    <section class="posts">
      <h1 class="post-title">{{loadedPost.title}}</h1>
      <div class="post-details">
        <div class="post-detail">最後更新日期：{{loadedPost.date}}</div>
        <div class="post-detail">發文人：{{loadedPost.author}}</div>
      </div>
      <p class="post-content">{{loadedPost.content}}</p>
    </section>
    <secton>
      <p class="post-feedback">
        讓我知道您對於這篇文章的看法，請寄信到
        <a href="mailto:feake@gmail.com">feake@gmail.com</a>
      </p>
    </secton>
  </div>
</template>

<script>
export default {
  async asyncData(context) {
    return await new Promise((resolve, reject) =>
      setTimeout(
        () =>
          resolve({
            loadedPost: {
              id: "1",
              title: "第一篇文章(ID:" + context.route.params.id + ")",
              date: new Date(),
              content:
                "不是很懂context用法，這邊是連接context，之後需要再了解。",
              author: "Len",
            },
          }),
        1000
      )
    );
  },
};
</script>


<style scoped>
.single-post-page {
  padding: 30px;
  text-align: center;
  box-sizing: border-box;
}

.post {
  width: 100%;
}

@media (min-width: 768px) {
  .post {
    width: 600px;
    margin: auto;
  }
}

.post-title {
  margin: 0;
}

.post-details {
  padding: 10px;
  box-sizing: border-box;
  border-bottom: 3px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 768px) {
  .post-details {
    flex-direction: row;
  }
}

.post-detail {
  color: rgb(88, 88, 88);
  margin: 0 10px;
}

.post-feedback a {
  color: red;
  text-decoration: none;
}

.post-feedback a:hover,
.post-feedback a:active {
  color: salmon;
}
</style>
