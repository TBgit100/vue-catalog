<template>
  <div class="v-cart-item">
    <img
     class="v-catalog-item__image"
     :src="require('../assets/images/' + cart_item_data.image)" 
     alt="picture"
     >
     <div>
      <p>{{cart_item_data.name}}</p>
      <p>{{cart_item_data.price}}</p>
      <p>{{cart_item_data.article}}</p>
      <p>{{cart_item_data.about}}</p>
     </div>
     <div class="v-cart-item__quantity">
        <div>
          <p>Quantity</p>
          <span>
            {{ cart_item_data.quantity }}
          </span>
        </div>
        <button @click="deleteFromCart">Delete</button>
     </div>
  </div>
</template>

<script>
export default {
    name: 'v-cart-item',
    props: {
      cart_item_data:{
        type: Object,
        default(){
                return {};
            }
      }
    },
    data(){
        return{}
    },
    methods: {
      deleteFromCart(){
        this.$emit("deleteFromCart");
      }
    }

}
</script>

<style scoped>
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

    .v-cart-item__quantity{
      display: flex;
      align-items: center;
    }

    .v-catalog-item__image{
      margin: 0;
    }
</style>