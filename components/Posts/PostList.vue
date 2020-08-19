<template>
  <section class="posts-list">
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU"
      title="YOO!"
      previewText="第一篇文章"
    />
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU"
      title="YOO!"
      previewText="第二篇文章"
    />
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      thumbnail="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU"
      title="YOO!"
      previewText="第三篇文章"
    />
  </section>
</template>

<script>
import PostPreview from "../../components/Posts/PostPreview";

export default {
  components: {
    PostPreview,
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false,
    },
  },
};
</script>


<style scoped>
.posts-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>

