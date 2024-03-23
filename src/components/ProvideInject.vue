<template>
    <div>
        <h3>Parent component {{ name }}</h3>
        <h3>Parent component count {{ count }}</h3>
        <h3>Parent component hero {{ firstName }} {{ lastName }}</h3>

        <button @click="incrementCount">Increment count</button>
        <button @click="decrementCount">Decrement count</button>

        <ChildA />
    </div>
</template>

<script>
import { provide, ref, reactive, toRefs } from 'vue'
import ChildA from './ChildA.vue'

    export default {
        name: 'ProvideInject',
        components: { ChildA },
        setup() {
            provide('c_userName', 'Codevolution')

            function incrementCount() {
                count.value ++
            }

            function decrementCount() {
                count.value --
            }

            const count = ref(0)
            const state = reactive({
                firstName: 'Bruce',
                lastName: 'Wayne',
            })

            provide('c_count', count)
            provide('c_hero', state)
            provide('incrementCount', incrementCount)
            provide('decrementCount', decrementCount)

            return {
                count,
                ...toRefs(state),
                incrementCount,
                decrementCount
            }
        },
        data() {
            return {
                name: 'Vishwas',
            }
        },
        provide() {
            return {
                userName: this.name,
            }
        }
    }
</script>

<style scoped>

</style>