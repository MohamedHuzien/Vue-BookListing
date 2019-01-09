<template>
    <form v-on:submit.prevent="bookSubmit(bookTitle,bookAuther)" class="" action="#" method="post">
    <input v-model="bookTitle" type="text" name="title" value="" placeholder="Book Title">
    <input v-model="bookAuther" type="text" name="author" value="" placeholder="Book Author">
    <button  type="submit" name="button">Add Book</button>
</form>
</template>

<script>
export default {
    name: 'BookForm',
    'props': ['books'],
    data() {
        return {
            bookTitle: '',
            bookAuther: ''
        }
    },
    methods: {
        bookSubmit : function(bookTitle, bookAuther) {
            this.$emit('addBook', bookTitle, bookAuther);
        }
    }
}
</script>

<style>

</style>
