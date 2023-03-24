<script>
import CardElement from './CardElement.vue';

export default {
    name: 'MainComicsList',
    components: {
        CardElement
    },
    data() {
        return {
            comicsList: [
                {
                    "thumb": "https://cdn.vox-cdn.com/thumbor/XrzeGSyhIupLQs86I12Xj5XAWS8=/1400x1400/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/21997971/jbareham_201027_0988_grids_superman_vrs02.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://i1.wp.com/multiversitystatic.s3.amazonaws.com/uploads/2020/07/American-Vampire-1976-issue-1-featured.jpg?fit=1000%2C1000",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://cdn.shopify.com/s/files/1/0575/3543/0796/products/a_main__76269.1616023858.1280.1280.jpg?v=1654972441",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://i.scdn.co/image/ab67706c0000da843ca4703c7e674aeeeac293dd",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://bleedingcool.com/wp-content/uploads/2018/10/STL097095-900x900.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/calendari/batman-comics-i143444.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/W/IMAGERENDERING_521856-T1/images/I/71AWCYyJuWL._SY300_.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://images.everyeye.it/img-notizie/batman-superman-uniscono-forze-serie-dc-comics-v5-558652-1200x1200.webp",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.dc.com/dc/files/default_images/SeriesThumb7_BMJokerWarZone_5f652a2a5f1018.39703665.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://assets.reedpopcdn.com/Batman-%26-The-Joker-The-Deadly-Duo-1-1-(1).jpg/BROK/thumbnail/1200x1200/quality/100/Batman-%26-The-Joker-The-Deadly-Duo-1-1-(1).jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://bleedingcool.com/wp-content/uploads/2020/06/Eba8-tdXkAMqaHB-900x900.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://bleedingcool.com/wp-content/uploads/2018/07/STL086344-900x900.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
            <CardElement
            class="card"
            v-for="comic in comicsList"
            :img="comic.thumb"
            :title="comic.series"/>
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
        background-color: inherit;

        :deep(.img) {
            margin-bottom: 1.25rem;

            img {
                max-width: 100%;
                display: block;
            }
        }

        :deep(h3) {
            text-transform: uppercase;
            font-size: 0.9em;
            color: #fff;
            font-weight: 400;
        }
    }
}
</style>