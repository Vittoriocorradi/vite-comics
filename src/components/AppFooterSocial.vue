<script>
    export default {
        name: 'FooterSocial'
    }
</script>

<template>
    <section>
        <div class="container-big">
            <div>
                <button>
                    sign-up now!
                </button>
            </div>
            <div>

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
                    cursor: pointer;
                }
            }
        }
    }
    
</style>