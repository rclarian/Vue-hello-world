<template>
    <div>
        <button @click="incrementCount">Clicked {{ count }} times</button>
    </div>
</template>

<script>
//import CounterMixin from '../mixins/counter'
import useCounter from '../composables/useCounter'
    export default {
        name: 'ClickCounter',
        //mixins: [CounterMixin],
        setup() {
            const {count, incrementCount} = useCounter(100, 10)

            return {
                count,
                incrementCount
            }
        }
    }
</script>

<style scoped>

</style>