<script>
import CounterCards from './CounterCards.vue';
import CardsList from './CardsList.vue';
export default {
    name: 'MainBody',
    components: {
        CounterCards,
        CardsList
    }
}
</script>
<template>
    <div class="container p-5 bg-light">
        <CounterCards />
        <CardsList />
    </div>
</template>
