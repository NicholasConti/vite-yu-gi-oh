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
        <h4>{{ name }}</h4>
        <div>{{ type }}</div>
    </div>
</template>