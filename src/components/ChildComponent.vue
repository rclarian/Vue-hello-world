<template>
    <div>
        <div>Child Component</div>
    </div>
</template>

<script>
    export default {
        name: 'ChildComponent',
        beforeCreate() {
            console.log('1-Child beforeCreate()')
        },
        created() {
            console.log('2-Child created()')
        },
        beforeMount() {
            console.log('3-Child beforeMount()')
        },
        mounted() {
            console.log('4-Child mounted()')
        },
        beforeUpdate() {
            console.log('5-Child beforeUpdate()')
        },
        updated() {
            console.log('6-Child updated()')
        },
        beforeUnmount() {
            console.log('7-Child beforeUnmount()')
        },
        unmounted() {
            console.log('8-Child unmounted()')
        },
    }
</script>

<style scoped>

</style>