<template>
  <div class="single-post-page">
    <section class="posts">
      <h1 class="post-title">文章標題</h1>
      <div class="post-details">
        <div class="post-detail">最後更新日期：</div>
        <div class="post-detail">發文人：</div>
      </div>
      <p class="post-content">文章內容</p>
    </section>
    <secton>
      <p class="post-feedback">
        問題回報，信箱
        <a href="mailto:yohren00@gmail.com">yohren00@gmail.com</a>
      </p>
    </secton>
  </div>
</template>

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
