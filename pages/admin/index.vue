<template>
  <div class="admin-page">
    <section class="new-post">
      <AppButton @click="$router.push('/admin/new-post')">新增文章</AppButton>
    </section>
    <section class="existing-posts">
      <h1>編輯文章</h1>
      <ProstList isAdmin />
    </section>
  </div>
</template>

<script>
import ProstList from "@/components/Posts/PostList";
import AppButton from "@/components/UI/AppButton";

export default {
  layout: "admin",
  components: {
    ProstList,
    AppButton,
  },
};
</script>


<style scoped>
.admin-page {
  padding: 20px;
}

.new-post {
  text-align: center;
  border-bottom: 2px solid #ccc;
  padding-bottom: 10px;
}

.existing-posts h1 {
  text-align: center;
}
</style>
