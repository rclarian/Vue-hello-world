<template>
    <div>
        <h2>This is a Popup</h2>
        <button @click="$emit('close', 'Vishwas')">Close Popup</button>
    </div>
</template>

<script>
    export default {
        name: 'PopupComponent',
        emits: ['close']
    }
</script>

<style scoped>

</style>