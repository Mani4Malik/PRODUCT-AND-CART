<template>
        <div class="splash-container">
                <div class="splash">
                <h1>Splendid Food</h1>
                </div>
            </div>

            <main class="wrapper">

                <h2>Recommended</h2>

                <div class="recommended">

                <productCard class="card" 
                v-for="(product,index) in inventory.slice(0,3)"
                :key="product.id"
                :index="index"
                :product="product"
                :addToCart="addToCart"
                />              
                


                </div>

            </main>
</template>
<script>
import productCard from '@/components/productCard.vue';

export default {
     props:['inventory','addToCart'],

    name: 'HomeView',
    components:{
    productCard,
}
}

</script>
