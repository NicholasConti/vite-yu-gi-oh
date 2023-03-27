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
    <main class="bg-orange">
        <NavMain />
        <CardsMain />
    </main>
</template>
<style lang="scss" scoped></style>