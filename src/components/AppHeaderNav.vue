<script>
    export default {
        name: 'HeaderNav',
        data() {
            return {
                navList: [
                {
                    name: 'characters',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'comics',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'movie',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'tv',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'games',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'collectibles',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'videos',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'fans',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'news',
                    ref: '#',
                    destination: '_self'
                },
                {
                    name: 'shop',
                    ref: '#',
                    destination: '_self'
                },
                ]
            }
        }
    }
</script>

<template>
    <ul>
        <li v-for="item in navList">
            <a :href="item.ref" :target="item.destination">
                <span> {{ item.name }} </span>
            </a>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
    @use "./styles/general.scss" as *;
    @use "./styles/variables.scss" as *;

    ul {
        display: flex;
        list-style-type: none;
        li {
            height: 100%;
            
            a {
                display: inline-block;
                text-decoration: none;
                color: #464646;
                padding: 0 1.0625rem;
                text-transform: uppercase;
                font-size: 14px;
            }
            
            span {
                display: inline-block;
                padding: 3.25rem 0;
            }
            
            &:nth-child(2) span {
                border-bottom: .3125rem solid $primary-color;
                color: $primary-color;
            }
        }
    }
</style>