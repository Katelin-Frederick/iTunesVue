<template>
  <div id="app">
    <Header />
    <Form v-bind:searchResults="searchResults" v-on:set-search="setSearch" />
    <Table v-bind:searchResults="searchResults"/>
  </div>
</template>

<script>
import Header from './components/Header'
import Form from './components/Form'
import Table from './components/Table'

export default {
  name: 'app',
  components: {
    Header,
    Form,
    Table
  },
  data() {
    return {
      searchResults: []
    }
  },
  methods: {
    setSearch(data) {
      this.searchResults = data
    }
  }
}
</script>

<style>

</style>
