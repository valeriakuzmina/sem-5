<template>
<div>
<div class="product-details">
  <div  v-for="product in products" :key="product.id">
    <h1>{{ product.name }}</h1>
    <p>{{ getFormattedPrice(product.price) }}</p>
    <p>{{ getAvailabilityStatus(product.available) }}</p>
  </div>
  </div>
  </div>
</template>

<script>
export default {
  name: 'productDetails',
  data() {
    return {
      products: [
       {
        id: 1,
        name: 'shirt',
        price: 99.85,
        available: false
      },
       {
        id: 2,
        name: 'skirt',
        price: 99.99,
        available: true
      },
       {
        id: 3,
        name: 'baby',
        price: 70.50,
        available: true
      }
      ]
    };
  },
   methods: {
    getFormattedPrice(price) {
      return `$${price.toFixed(2)}`;
    },
    getAvailabilityStatus(available) {
      return available ? 'Available' : 'Out of stock';
    }
  }
};
</script>

<style>
.product-details{
  display: flex;
  justify-content: center;
  gap: 50px;
}
</style>