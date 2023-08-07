<template>
  <div class="v-cart-item">
    <p>item 1</p>
    <p>Price: 100</p>
    <button>Add to cart</button>
  </div>
</template>

<script>
export default {
    name: 'v-cart-item',
    props: {},
    data(){
        return{}
    }

}
</script>

<style>
    .v-cart-item{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        align-items: center;
        flex-basis: 25%;
        max-width: 900px;
        margin: 0 auto;
        box-shadow: 0 0 8px 0 grey;
        padding: 20px;
        margin: 20px;
    }
</style>