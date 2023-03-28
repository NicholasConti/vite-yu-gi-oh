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
            })
    }
}
</script>

<template>
    <AppHeader />
    <AppMainVue @filterCards="search" />
</template>

<style></style>
