<script>
    export default {
        name: 'MainComicsList'
    }
</script>

<template>
    <section>
        <div class="container">
            <div class="card">
                <div class="img">
                    img
                </div>
                <h3>
                    titolo
                </h3>
            </div>
        </div>
        <div>
            <button>load more</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../assets/styles/partials/mixins.scss' as *;

    section {
        background-color: #1c1c1c;
        padding: 3.4375rem 0 1.25rem;
    }

    .container {
        @include my-container(80rem);

        display: flex;
        flex-wrap: wrap;

        .card {
            width: calc(100% / 6 - 1.875rem);
            margin: 0 .9375rem 3.125rem;
            background-color: #fff;

            .img {
                margin-bottom: 1.25rem;

                img {
                    max-width: 100%;
                }
            }

            h3 {
                text-transform: uppercase;
            }
        }
    }
</style>