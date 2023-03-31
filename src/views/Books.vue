<template>
<div>
    <app-header title="Books" tooltip="Add Book" @add="$router.push('/books/0')" @search="searchInBooks($event)"/>
    <v-list three-line>
        <template v-for="(item, index) in books">
            <book-card :item="item" :key="item._id" @click="selectedBook(index, item._id)"></book-card>
        </template>
    </v-list>
</div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue'
import booksList from '@/data/books.json'
import BookCard from '@/components/Bookcard.vue'
export default {
    components: {
        AppHeader,
        BookCard
    },
    data() {
        return {
            books: booksList || []
        }
    },
    methods: {
        selectedBook(index, id) {
            this.$router.push('/books/view/'+id)
        },
        searchInBooks(searchText){
            console.log(searchText);
            if(searchText){
                this.books = booksList.filter(rec => rec.title.toLowerCase().includes(searchText.toLowerCase()))
            }
            else
                this.books = booksList
        }
    },
}
</script>

<style lang="scss" scoped>

</style>
