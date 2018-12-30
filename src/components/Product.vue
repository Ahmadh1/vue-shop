<template>
    <div class="card my-5">
        <div class="card-body">
            <h3 class="text-center card-title">{{ product.title }}</h3>
            <p class="text-center text-muted card-text display-4">${{ product.price }}</p>
            <button :disabled="isInCart" @click="$emit('add-to-cart', product)" class="btn btn-primary form-control">
                {{ isInCart ? 'Added to cart' : 'Add to cart' }}
            </button>
        </div>
    </div>
</template>

<script>
export default {

    props:['product', 'isInCart']

}
</script>

<style>

</style>
