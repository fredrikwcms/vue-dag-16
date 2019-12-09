<template>
    <article class="row">
        <div class="col-6">{{ articleTitle }}</div>
    </article>
</template>

<script>
export default {
    name: 'MyArticle',
    props: {
        articleTitle: String
    },
    data() {
        return {
        articleContent: 'Some content for our article!'
        }
    }
}
</script>

<style scoped>

</style>