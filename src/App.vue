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
    methods: {
        search() {
            if (store.archetype !== '') {
                axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
                    params: {
                        archetype: store.archetype
                    }
                })
                    .then((response) => {
                        this.store.cards = response.data.data;
                        this.store.counter = response.data.data.length;
                    })
            } else {
                axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
                    .then((response) => {
                        this.store.cards = response.data.data;
                        this.store.counter = response.data.data.length;
                    })
            }

        },
        listArchtypes() {
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
                .then((response) => {
                    this.store.selectArchtypes = response.data;
                    console.log(this.store.selectArchtypes);
                })
        }
    },
    created() {
        this.listArchtypes();
        this.search();
    }
}
</script>

<template>
    <AppHeader />
    <AppMainVue @filterCards="search" />
</template>

<style></style>
