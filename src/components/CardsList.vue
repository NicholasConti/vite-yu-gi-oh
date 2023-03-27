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
    <section class="px-3 row">
        <div class="col-3" v-for="card in store.cards">
            <SingleCard :img="card.card_images[0].image_url" :name="card.name" :type="card.type" />
        </div>
    </section>
</template>