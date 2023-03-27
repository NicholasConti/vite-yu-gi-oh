<script>
export default {
    name: 'Card',
    props: {
        img: String,
        name: String,
        type: String
    }
}
</script>

<template>
    <div>
        <div class="img"><img :src="img" class="img-fluid"></div>
        <div class="bg-orange">
            <h5>{{ name }}</h5>
            <div>{{ type }}</div>
        </div>
    </div>
</template>