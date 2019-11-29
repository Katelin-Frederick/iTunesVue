<template>
    <div>
        <div v-bind:key="searchResult.trackId" v-for="searchResult in searchResults">
            <SearchItem v-bind:searchResult="searchResult" />
        </div>
    </div>
</template>

<script>
import SearchItem from './SearchItem'

export default {
    name: 'Table',
    props: ["searchResults"],
    components: {
        SearchItem
    }
}
</script>

<style scoped>

</style>