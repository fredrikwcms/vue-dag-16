<template>
    <h1>{{ title }}</h1>
</template>

<script>
export default {
    name: 'MyTitle',
    props: {
        title: String
    }
}
</script>

<style scoped>
    h1 {
        color: red;
    }
</style>