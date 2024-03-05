<template>
    <div>
        <h2>Hello {{ name }} a.k.a {{ hero-name }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'GreetComponent',
        props: ['name', 'hero-name'],
    }
</script>

<style scoped>

</style>