<script>
import SingleCard from './SingleCard.vue';
import { store } from '../store';
export default {
    name: 'List',
    components: {
        SingleCard
    },
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <section class="px-3 row g-3">
        <div class="col-2 text-center" v-for="card in store.cards.slice(0, 40)">
            <SingleCard :img="card.card_images[0].image_url_small" :name="card.name" :type="card.archetype" />
        </div>
    </section>
</template>