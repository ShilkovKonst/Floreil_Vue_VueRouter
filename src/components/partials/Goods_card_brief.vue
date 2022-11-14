<template>
    <div class="col-12 col-md-6 col-lg-4">

        <div class="card mb-3" style="max-width: 540px;">
            <div class="row">
                <h5 class="card-title">{{ title }}</h5>
            </div>
            <div class="row g-0">
                <div class="col-md-4">
                    <RouterLink :to='`${id}`'>
                        <img :src="`./data_goods_images/${image}`" class="img-fluid rounded-start" :alt=image>
                    </RouterLink>
                    <ul>
                        <li>
                            <p>Prix: <br><span>{{ price }}</span>  &#8364</p>
                        </li>
                        <li>
                            <p>Quantité: <br><span>{{ quantity }}</span></p>
                        </li>
                    </ul>
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <ul>
                            <li>
                                <p>Nom commun: <span>{{ Nom_commun }}</span></p>
                            </li>
                            <li>
                                <p>Genre de la plante: <span>{{ Genre_de_la_plante }}</span></p>
                            </li>
                            <li>
                                <p>Espèce: <span>{{ Espèce }}</span></p>
                            </li>
                            <li>
                                <p>Variété: <span>{{ Variété }}</span></p>
                            </li>
                            <li>
                                <p>Famille: <span>{{ Famille }}</span></p>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { RouterLink } from 'vue-router'

export default {
    name: "Goods_card_brief",
    props: {
        id: Number,
        type: String,
        image: String,
        title: String,
        Nom_commun: String,
        Genre_de_la_plante: String,
        Espèce: String,
        Variété: String,
        Famille: String,
        link: String,
        price: Number,
        quantity: Number
    },
    data(){
        return {
        }
    }
}
</script>