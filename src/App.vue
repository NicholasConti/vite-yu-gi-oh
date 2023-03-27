<script>
import axios from 'axios';
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import AppMainVue from './components/AppMain.vue';
export default {
    components: {
        AppHeader,
        AppMainVue
    },
    data() {
        return {
            store
        }
    },
    created() {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
            .then((response) => {
                this.store.cards = response.data.data;
                this.store.maxShow = this.store.cards.slice(0, 40);
                console.log(this.store.maxShow);
            })
    }
}
</script>

<template>
    <AppHeader />
    <AppMainVue />
</template>

<style></style>
