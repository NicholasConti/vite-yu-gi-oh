<script>
import { store } from '../store';
export default {
    name: 'Nav',
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <div class="container p-4">
        <select v-model="store.archetype" @change.prevent="$emit('selectArchtype')">
            <option selected value="">Select an archetype</option>
            <option>Crystal Beast</option>
            <option>Elemental HERO</option>
            <option>Blue-Eyes</option>
        </select>
    </div>
</template>