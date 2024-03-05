<template>
    <div>
        <h2>ComponentsC</h2>
        <ComponentsE />
    </div>
</template>

<script>
import ComponentsE from './ComponentsE.vue';
    export default {
        name: 'ComponentsC',
        components: {
            ComponentsE,
        }
    }
</script>

<style scoped>

</style>