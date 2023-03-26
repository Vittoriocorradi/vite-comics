<script>
    export default {
        name: 'HeaderNav',
        data() {
            return {
                navList: [
                {
                    name: 'characters',
                    ref: '#',
                    destination: '_self',
                    isActive: true
                },
                {
                    name: 'comics',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'movie',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'tv',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'games',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'collectibles',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'videos',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'fans',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'news',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                {
                    name: 'shop',
                    ref: '#',
                    destination: '_self',
                    isActive: false
                },
                ]
            }
        },
        methods: {
            activeItem(i) {
                this.navList.forEach((el, index) => {
                    if (i === index) {
                        el.isActive = true;
                    } else {
                        el.isActive = false;
                    }
                })
            }
        }
    }
</script>

<template>
    <ul>
        <li v-for="(item, index) in navList">
            <a :href="item.ref" :target="item.destination" @click.prevent="activeItem(index)">
                <span :class="{active: item.isActive}"> {{ item.name }} </span>
            </a>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
    @use "../assets/styles/partials/mixins" as *;
    @use "../assets/styles/partials/variables.scss" as *;

    ul {
        display: flex;
        list-style-type: none;
        li {
            height: 100%;
            transition: background-color 0.2s;
            
            &:hover {
                background-color: lighten($primary-color, 40%);
            }
            
            a {
                display: inline-block;
                text-decoration: none;
                color: #464646;
                font-weight: 700;
                padding: 0 1.0625rem;
                text-transform: uppercase;
                font-size: 14px;

            }
            
            span {
                display: inline-block;
                padding: 3.25rem 0;
            }
            
            .active {
                border-bottom: .3125rem solid $primary-color;
                color: $primary-color;
                padding-bottom: 2.9375rem;
            }
        }
    }
</style>