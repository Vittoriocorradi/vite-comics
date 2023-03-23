<script>
    export default {
        name: 'FooterNav',
        data() {
            return {
                navList: [
                    {
                        link: 'buy-comics-digital-comics.png',
                        title: 'digital comics',
                        ref: '#',
                        destination: '_self'
                    },
                    {
                        link: 'buy-comics-merchandise.png',
                        title: 'dc merchandise',
                        ref: '#',
                        destination: '_self'
                    },
                    {
                        link: 'buy-comics-subscriptions.png',
                        title: 'subscription',
                        ref: '#',
                        destination: '_self'
                    },
                    {
                        link: 'buy-comics-shop-locator.png',
                        title: 'comic shop locator',
                        ref: '#',
                        destination: '_self'
                    },
                    {
                        link: 'buy-dc-power-visa.svg',
                        title: 'dc power visa',
                        ref: '#',
                        destination: '_self'
                    },
                ]
            }
        }
    }
</script>

<template>
    <section class="footer-nav">
        <ul class="container-mid">
            <li v-for="item in navList">
                <a :href="item.ref" :target="item.destination">
                    <div class="link">
                        <div class="img">
                            <img :src="'/src/assets/' + item.link" :alt="item.title">
                        </div>
                        <div>
                            {{ item.title }}
                        </div>
                    </div>
                </a>
            </li>
        </ul>
    </section>
</template>

<style lang="scss" scoped>
    @use "./styles/general.scss" as *;
    @use "./styles/variables.scss" as *;

    section {
        background-color: $primary-color;

        .container-mid {
            @include my-container(75rem);
            @include my-flex(flex, space-between, center);
            list-style-type: none;
        }

            li {

                a {
                    display: inline-block;
                    padding: 3.125rem .625rem;
                    text-decoration: none;

                    .link{
                        @include my-flex(flex, start, center);

                        .img {
                            height: 3.4375rem;
                            margin-right: .9375rem;

                            img {
                                height: 100%;
                            }
                        }

                        & div:last-child {
                            color: #fff;
                            text-transform: uppercase;
                            font-size: .875rem;
                        }
                    }
                }
            }
    }
</style>