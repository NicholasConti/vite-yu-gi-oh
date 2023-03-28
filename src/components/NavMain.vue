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
            <option v-for="(type, index) in store.selectArchtypes.slice(0, 30)">{{ type.archetype_name }}</option>
        </select>
    </div>
</template>