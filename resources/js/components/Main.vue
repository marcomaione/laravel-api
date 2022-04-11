<template>
  <h1>  Elenco dei post</h1>
</template>

<script>
export default {
    name: 'Main',

    data() {
        return {
            posts:[]
        }
    },

    created() {
        axios.get('/api/posts').then((response)=> {
            this.posts = response.data.results;
        });
    }

}
</script>

<style>

</style>