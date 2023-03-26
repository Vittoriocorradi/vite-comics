<script>
    import Price from './Price.vue';

    export default {
        name: 'Card',
        props: {
            img: String,
            title: String,
            price: String,
            isShown: Boolean
        },
        components: {
            Price
        },
        methods: {
            myConsoleLog() {
                console.log(this.isShown);
            }
        },
        mounted() {
            this.myConsoleLog();
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
        :class="{'is-shown': !isShown}"
        />
    </div>
</template>

<style lang="scss" scoped>
    .is-shown {
        visibility: hidden;
    }
</style>