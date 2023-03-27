<script>
import NavMain from './NavMain.vue';
import CardsMain from './CardsMain.vue';
export default {
    name: 'Main',
    components: {
        NavMain,
        CardsMain
    }
}
</script>
<template>
    <main>
        <NavMain />
        <CardsMain />
    </main>
</template>
<style lang="scss" scoped>
main {
    background-color: #d48f38;
}
</style>