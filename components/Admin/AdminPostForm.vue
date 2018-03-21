<template>
  <form @submit.prevent="onSave">
    <!-- <AppControlInput v-model="editedPost.author">Author Name</AppControlInput> -->
    <AppControlInput v-model="editedPost.title">Title</AppControlInput>
    <AppControlInput
      control-type="textarea"
      v-model="editedPost.text">Text</AppControlInput>
    <AppControlInput v-model="editedPost.thumbnail">Thumbnail Link</AppControlInput>
    <AppControlInput
      control-type="input"
      v-model="editedPost.link.href">Button Link</AppControlInput>
    <AppControlInput
      control-type="input"
      v-model="editedPost.link.key">Button Text</AppControlInput>
    <AppButton type="submit">Save</AppButton>
    <AppButton
      type="button"
      style="margin-left: 10px"
      btn-style="cancel"
      @click="onCancel">Cancel</AppButton>
  </form>
</template>

<script>
import AppControlInput from '@/components/UI/AppControlInput';
import AppButton from '@/components/UI/AppButton';

export default {
  components: {
    AppControlInput,
    AppButton
  },
  props: {
    post: {
      type: Object,
      required: false
    }
  },
  data() {
    return {
      editedPost: this.post
        ? { ...this.post }
        : {
            // author: '',
            title: '',
            text: '',
            thumbnail: '',
            link: {
              '': '',
              '': ''
            }
            // previewText: ''
          }
    };
  },
  methods: {
    onSave() {
      // Save the post
      this.$emit('submit', this.editedPost);
    },
    onCancel() {
      // Navigate back
      this.$router.push('/admin');
    }
  }
};
</script>
