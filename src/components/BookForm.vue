<template>
  <form action="#" v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)" method="post">
    <input v-model="bookTitle" type="text" name="bookTitle" placeholder="Book Name">
    <input v-model="bookAuthor" type="text" name="bookAuthor" placeholder="Book Author">
    <button type="submit"> Add Book</button>

  </form>

</template>

<script>
  export default {
    name: 'BookForm',
    props: ['books'],
    data() {
      return {
        bookTitle: '',
        bookAuthor: ''
      };
    },
    methods: {
      bookSubmit(bookTitle, bookAuthor){
        this.$emit('addBook', bookTitle, bookAuthor)
      }
    }
  };
</script>

<style scoped>


</style>
