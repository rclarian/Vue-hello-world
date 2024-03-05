<template>
    <div>
        <h2>ComponentsF</h2>
        <h2>Components F username {{ username }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'ComponentsF',
        inject: ['username'] //step 2
    }
</script>

<style scoped>

</style>