<template>
    <div class="column is-3">
        <div id='black-box' class="box has-background-dark">
            <figure class="image mb-3">
                <img id='image' v-bind:src="product.get_thumbnail">                 
            </figure>
            <div> 
                <h3 class="is-size-4 has-text-light">{{ product.name }}</h3>
                <p class="is-size-6 has-text-light">Rs {{ product.price }}</p>
            </div>

            <router-link v-bind:to="`/${product.get_absolute_url}`" class="button is-light mt-4" v-bind:product="product">View details</router-link>
        </div>
    </div>


</template>

<script>
export default {
    name: 'ProductBox',
    props: {
        product: Object
    }
}
</script>

<style scoped>
 #black-box {
    height:100%;
 }
 #image {
    height: 35rem;
 }
  .image {
    margin-top: -1.25rem;
    margin-left: -1.25rem;
    margin-right: -1.25rem;
  }
</style>