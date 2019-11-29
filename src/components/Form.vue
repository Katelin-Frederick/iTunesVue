<template>
    <form @submit="onSubmit">
        <input type="text" v-model="searchTerm" name="searchTerm" placeholder="Search for Song or Artist...">
        <input type="submit" value="Submit">
    </form>
</template>

<script>
export default {
    name: 'Form',
    props: ["searchResults"],
    data() {
        return {
            searchTerm: ''
        }
    },
    methods: {
        onSubmit(e) {
            e.preventDefault()

            fetch(`https://itunes.apple.com/search?term=${this.searchTerm}&kind=song`)
                .then(res => res.json())
                .then(data => this.$emit('set-search', data.results))

            this.searchTerm = ''
        }
    }
}
</script>

<style scoped>

</style>