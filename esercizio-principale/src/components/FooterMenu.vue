<script>
    export default {
        name: 'FooterMenu',
        data() {
            return {
                lists: [
                    {
                        title: 'dc comics',
                        listItems: [
                            'Characters',
                            'Comics',
                            'Movies',
                            'TV',
                            'Games',
                            'Videos',
                            'News'
                        ]
                    },
                    {
                        title: 'shop',
                        listItems: [
                            'Shop DC',
                            'Shop DC Collectibles'
                        ]
                    },
                    {
                        title: 'dc',
                        listItems: [
                            'Terms Of Use',
                            'Privacy Policy (New)',
                            'Ad Choices',
                            'Advertising',
                            'Jobs',
                            'Subscriptions',
                            'Talent Workshop',
                            'CPSC Certificates',
                            'Ratings',
                            'Shop Help',
                            'Contact Us'
                        ]
                    },
                    {
                        title: 'sites',
                        listItems: [
                            'DC',
                            'MAD Magazine',
                            'DC Kids',
                            'DC Universe',
                            'DC Power Visa'
                        ]
                    },
                ]
            }
        }
    }
</script>

<template>
    <section class="background">
        <div class="container-big">
            <div>
                <h1>
                    {{ lists[0].title }}
                </h1>
                <ul>
                    <li v-for="item in lists[0].listItems">
                        <a href="#" target="_self"> {{ item }}</a>
                    </li>
                </ul>
                <h1>
                    {{ lists[1].title }}
                </h1>
                <ul>
                    <li v-for="item in lists[1].listItems">
                        <a href="#" target="_self"> {{ item }}</a>
                    </li>
                </ul>
            </div>
            <div>
                <h1>
                    {{ lists[2].title }}
                </h1>
                <ul>
                    <li v-for="item in lists[2].listItems">
                        <a href="#" target="_self"> {{ item }}</a>
                    </li>
                </ul>
            </div>
            <div>
                <h1>
                    {{ lists[3].title }}
                </h1>
                <ul>
                    <li v-for="item in lists[3].listItems">
                        <a href="#" target="_self"> {{ item }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @import '../assets/styles/partials/mixins.scss';
    .background {
        background-image: url('../assets/img/dc-logo-bg.png'), url('../assets/img/footer-bg.jpg');
        background-size: auto, cover;
        background-repeat: no-repeat;
        background-position-y: 60%, 0;
        background-position-x: 85%, 0;
    }

    .container-big {
        @include my-container(80rem);
        display: flex;
        padding: 1.5625rem 0 3.75rem;

        div {
            
            h1 {
                text-transform: uppercase;
                color: #fff;
                font-size: 1.2em;
                margin: 1.25rem 0;
            }

            ul {
                list-style-type: none;

                li {
                    margin-right: 1.875rem;

                    a {
                        display: inline-block;
                        text-decoration: none;
                        color: #959595;
                        padding: .125rem 0;
                        font-size: .8125rem;

                        &:hover {
                            text-decoration: underline;
                        }
                    }
                }
            }
        }
    }
</style>