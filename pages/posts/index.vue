<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "../../components/Posts/PostList";

export default {
  components: {
    PostList,
  },
  async asyncData(context) {
    await new Promise((resolve, reject) =>
      setTimeout(() => resolve(), 1000)
    ).catch((e) => {
      context.error(new Error());
    });

    return {
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
    };
  },
};
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>

