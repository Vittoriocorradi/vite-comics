<script>
    import Price from './Price.vue';

    export default {
        name: 'Card',
        props: {
            img: String,
            title: String,
            price: String
        },
        components: {
            Price
        }
    }
</script>

<template>
    <div>
        <div class="img">
            <img :src="img" :alt="title">
        </div>
        <h3>
            {{ title }}
        </h3>
        <Price
        :price="price"
        />
    </div>
</template>

<style lang="scss" scoped>

</style>