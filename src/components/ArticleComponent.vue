<template>
    <div>
        <h2>Article component</h2>
        <h2 :="$attrs">Title - {{ title }}</h2>
        <h2>Likes - {{ likes }}</h2>
        <h2>IsPublished - {{ isPublished ? 'Yes' : 'No' }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'ArticleComponent',
        props: {
            title: {
                type: String,
                required: true,
                default: 'Article default title'
            },
            likes: Number,
            isPublished: Boolean,
        },
        inheritAttrs: false,
    }
</script>

<style scoped>

</style>