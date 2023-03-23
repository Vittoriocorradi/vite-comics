<script>
    export default {
        name: 'FooterSocial',
        data() {
            return {
                icons: [
                    {
                        link: 'footer-facebook.png',
                        alt: 'Facebook logo'
                    },
                    {
                        link: 'footer-twitter.png',
                        alt: 'Twitter logo'
                    },
                    {
                        link: 'footer-youtube.png',
                        alt: 'Youtube logo'
                    },
                    {
                        link: 'footer-pinterest.png',
                        alt: 'Pinterest logo'
                    },
                    {
                        link: 'footer-periscope.png',
                        alt: 'Periscope logo'
                    }
                ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="container-big">
            <div class="button">
                <button>
                    sign-up now!
                </button>
            </div>
            <div class="icons-group">
                <div class="follow-us">
                    follow us
                </div>
                <div v-for="icon in icons" class="icon">
                    <a href="#">
                        <img :src="'/src/assets/' + icon.link" :alt="icon.alt">
                    </a>
                </div>
            </div>
        </div>
    </section>
    
</template>

<style lang="scss" scoped>
    @use "./styles/general.scss" as *;
    @use "./styles/variables.scss" as *;
    section {
        background-color: #303030;
        .container-big {
        @include my-container(80rem);
        @include my-flex(flex, space-between, center);
        padding: 1.875rem 0;
        
            div:first-child {

                button {
                    display: block;
                    padding: .9375rem;
                    border: .125rem solid $primary-color;
                    color: #fff;
                    background-color: inherit;
                    text-transform: uppercase;
                    font-family: inherit;
                    cursor: pointer;
                }
            }
            .icons-group {
                margin-left: auto;
                @include my-flex(flex, center, center);

                .follow-us {
                    text-transform: uppercase;
                    color: $primary-color;
                    margin-right: .625rem;
                    font-weight: 900;
                }

                .icon {
                    margin-left: 1.125rem;
                }


            }
        }
    }
</style>