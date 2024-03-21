<template>
    <div>
        Parent Component
        <button @click="showChild = !showChild">Toggle Child</button>
        <ChildComponent v-if="showChild" />
    </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';
    export default {
        name: 'ParentComponent',
        components: { ChildComponent },
        data() {
            return {
                showChild: true,
            }
        },
        beforeCreate() {
            console.log('1-Parent beforeCreate()')
        },
        created() {
            console.log('2-Parent created()')
        },
        beforeMount() {
            console.log('3-Parent beforeMount()')
        },
        mounted() {
            console.log('4-Parent mounted()')
        },
        beforeUpdate() {
            console.log('5-Parent beforeUpdate()')
        },
        updated() {
            console.log('6-Parent updated()')
        },
        beforeUnmount() {
            console.log('7-Parent beforeUnmount()')
        },
        unmounted() {
            console.log('8-Parent unmounted()')
        },
    }
</script>

<style scoped>

</style>