<script>
import { store } from '../store';
export default {
    name: 'Counter',
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <div class="p-3 bg-dark text-white">COUNTER: {{ store.counter }}</div>
</template>