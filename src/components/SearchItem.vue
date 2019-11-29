<template>
    <div>
        <h2 v-text="searchResult.artistName"></h2>
        <p v-text="searchResult.collectionName"></p>
        <p v-text="searchResult.primaryGenreName"></p>
        <img v-bind:src="searchResult.artworkUrl100" alt="Album Artwork">
    </div>
</template>

<script>
export default {
    name: 'SearchItem',
    props: ['searchResult']
}
</script>

<style scoped>

</style>