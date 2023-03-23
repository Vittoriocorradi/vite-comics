<script>
    export default {
        name: 'HeaderNav',
        data() {
            return {
                navList: [
                {
                    name: 'characters',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'comics',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'movie',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'tv',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'games',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'collectibles',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'videos',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'fans',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'news',
                    link: '#',
                    destination: '_self'
                },
                {
                    name: 'shop',
                    link: '#',
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
            <a :href="item.link" :target="item.destination">{{ item.name }}</a>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
    @use "../components/styles/general.scss" as *;
    @use "../components/styles/variables.scss" as *;

    ul {
        display: flex;
        list-style-type: none;
        li {
            height: 100%;
            a {
                display: inline-block;
                text-decoration: none;
                color: #464646;
                padding: 3.25rem 1.0625rem;
            }
            &:nth-child(2) a {
                border-bottom: .3125rem solid $primary-color;
                color: $primary-color;
            }
        }
    }
</style>