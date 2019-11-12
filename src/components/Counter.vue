<template>
    <div>
        <h2>{{ msg }}: {{ tripleCounter }}</h2>
        <increment/>
        <decrement/>
    </div>
</template>

<script>
import { mapGetters } from 'vuex'
import increment from './Increment.vue'
import decrement from './Decrement.vue'

export default {
    components: {
        increment,
        decrement
    },
    computed: {
        ...mapGetters(['tripleCounter']),
        msg() {
            return 'El contador multiplicado por 3 vale'
        }
    }
}
</script>

