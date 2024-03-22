<template>
    <div>
        <h2>{{ name }}</h2>
        <button @click="setName">Change Name</button>

        <h2>{{ count }}</h2>
        <button @click="incrementCount">Increment Count</button>

        <h2>{{ firstName }} {{ lastName }}</h2>
        <button @click="changeHero">Change Hero</button>
    </div>
</template>

<script>
import { ref, reactive, toRefs } from 'vue';
    export default {
        name: 'MethodsC',
        setup() {
            const count = ref(0)

            function incrementCount(){
                count.value ++
            }

            const state = reactive({
                firstName: 'Bruce',
                lastName: 'Wayne',
            })

            function changeHero(){
                state.firstName = 'Clark'
                state.lastName = 'Kent'
            }

            return {
                count,
                incrementCount,
                ...toRefs(state),
                changeHero
            }
        },
        data() {
            return {
                name: 'Vishwas',
            }
        },
        methods: {
            setName() {
                this.name = 'Codevolution'
            }
        }
    }
</script>

<style scoped>

</style>