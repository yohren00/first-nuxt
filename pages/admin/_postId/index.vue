<template>
  <div class="update-form">
    <AdminPostForm :post="loadedPost" />
  </div>
</template>

<script>
import AdminPostForm from "@/components/Admin/AdminPostForm";

export default {
  components: {
    AdminPostForm,
  },
  data() {
    return {
      loadedPost: {
        author: "Len",
        title: "我看不懂Vue",
        thumbnailLink:
          "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwQyAEDXUKgJ9JCNhfuCXnQbopPANbquVcPw&usqp=CAU",
        content: "這教學影片還是要有點vue的程度比較看得懂嗚嗚。",
      },
    };
  },
};
</script>


