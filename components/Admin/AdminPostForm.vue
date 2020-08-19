<template>
  <div class="update-form">
    <section class="new-post-form">
      <form @submit.prevent="onSave">
        <AppControlInput v-model="editedPost.author">發文者</AppControlInput>
        <AppControlInput v-model="editedPost.title">標題</AppControlInput>
        <AppControlInput v-model="editedPost.thumbnailLink">縮圖連結</AppControlInput>
        <AppControlInput control-type="textarea" v-model="editedPost.content">內容</AppControlInput>
        <AppButton type="submit">儲存</AppButton>
        <AppButton type="button" style="margin-left: 10px" btn-style="cancel" @click="onCancel">離開</AppButton>
      </form>
    </section>
  </div>
</template>

<script>
import AppControlInput from "@/components/UI/AppControlInput";
import AppButton from "@/components/UI/AppButton";

export default {
  components: {
    AppControlInput,
    AppButton,
  },
  props: {
    post: {
      type: Object,
      required: false,
    },
  },
  data() {
    return {
      editedPost: this.post
        ? { ...this.post }
        : {
            author: "",
            title: "",
            thumbnailLink: "",
            content: "",
          },
    };
  },
  methods: {
    onSave() {
      console.log(this.editedPost);
    },
    onCancel() {
      this.$router.push("/admin");
    },
  },
};
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}

@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>
