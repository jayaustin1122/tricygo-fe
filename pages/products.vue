<template>
    <div>
      <h2>Products</h2>
      <div class="product-list">
        <div
          class="product-card justify-center"
          v-for="(product, index) in products"
          :key="index"
          @click="selectProduct(product)"
        >
          <h3>{{ product.name }}</h3>
          <p>{{ product.description }}</p>
          <p>Price: ${{ product.price }}</p>
          <p>Quantity available: {{ product.quantity }}</p>
          <v-btn rounded color="primary">ORDER </v-btn>
      
        </div>
      </div>
  
      <h2>Order Details</h2>
      <div v-if="selectedProduct">
        <div class="card">
          <h3>{{ selectedProduct.name }}</h3>
          <p>Description: {{ selectedProduct.description }}</p>
          <p>Price: ${{ selectedProduct.price }}</p>
          <p>Quantity available: {{ selectedProduct.quantity }}</p>
        </div>
  
        <h2>User Details</h2>
        <div class="card">
          <div>
            <label for="name">Name:</label>
            <input type="text" id="name" v-model="userDetails.name">
          </div>
          <div>
            <label for="email">Email:</label>
            <input type="email" id="email" v-model="userDetails.email">
          </div>
          <div>
            <label for="address">Address:</label>
            <input type="text" id="address" v-model="userDetails.address">
          </div>
        </div>
  
        <h2>Delivery Location</h2>
        <div class="card">
          <input type="text" v-model="deliveryLocation" placeholder="Enter delivery location">
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        products: [
          { name: "Product 1", description: "Description 1", price: 10.00, quantity: 2 },
          { name: "Product 2", description: "Description 2", price: 15.00, quantity: 1 },
          { name: "Product 3", description: "Description 3", price: 20.00, quantity: 3 }
        ],
        selectedProduct: null,
        userDetails: {
          name: "",
          email: "",
          address: ""
        },
        deliveryLocation: ""
      };
    },
    methods: {
      selectProduct(product) {
        if (this.selectedProduct === product) {
          // If the same product is clicked again, close the user details
          this.selectedProduct = null;
        } else {
          this.selectedProduct = product;
        }
      }
    }
  };
  </script>
  
  
  <style scoped>
  .product-list {
    display: flex;
    flex-wrap: wrap;
  }
  
  .product-card {
    width: 300px;
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 16px;
    margin: 8px;
    cursor: pointer;
  }
  
  .card {
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 16px;
    margin-bottom: 16px;
  }
  </style>
  