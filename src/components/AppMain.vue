<script>
import NavMain from './NavMain.vue';
import CardsMain from './CardsMain.vue';
export default {
    name: 'Main',
    components: {
        NavMain,
        CardsMain
    },
    methods: {
        handleSearch() {
            console.log('ho ascoltato questo evento');
            this.$emit('filterCards');
        }
    }
}
</script>
<template>
    <main class="bg-orange">
        <NavMain @selectArchtype="handleSearch" />
        <CardsMain />
    </main>
</template>
<style lang="scss" scoped></style>