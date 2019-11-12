<template>
    <div id="app" class="container">
        <h1>Vuex</h1>
        <counter/>

        <p>El contador es: {{ count }} y el contador multiplicado por 3 es: {{ tripleCounter }}</p>
    </div>
</template>

<script>
import store from './store'
import { mapGetters } from 'vuex'
import Counter from './components/Counter.vue'

export default {
    name: 'app',
    components: {
        'counter': Counter
    },
    computed: {
        ...mapGetters(['tripleCounter']),
        count() {
            return store.state.count
        }
    }
}
</script>

<style lang="scss">
    @import '~bootstrap/scss/bootstrap';
</style>
