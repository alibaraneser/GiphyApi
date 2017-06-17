<template>
    <div class="search">
        <input type="text" v-model="query" @keypress.enter="handleSearch">
        <button v-on:click="handleSearch">Search</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            query : ''
        }
    },
    methods : {
        handleSearch () {
            this.$emit('SearchRequested',this.query);
        }
    }
}
</script>

<style>
    .search {
        margin : 20px;
    }
</style>