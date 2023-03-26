<script>
    export default {
        name: 'Price',
        props: {
            price: String
        }
    }
    
</script>

<template>
    <small> {{ price }} </small>
</template>