<script>
    export default {
        name: 'Card',
        props: {
            img: String,
            title: String
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
    </div>
</template>