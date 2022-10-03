<template>
  <div class="home">
    <Navbb />
    <div class="container">
      <div class="mb-2">
        <HerBan />
      </div>

      <div class="row mt-4">
        <div class="col">
          <h2><strong>Best</strong> Sellers</h2>
        </div>
        <div class="col">
          <router-link to="/products" class="btn btn-primary float-right">
            <b-icon-bag></b-icon-bag> Shop Now
          </router-link>
        </div>
      </div>

      <div class="row mb-3">
        <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
          <CardProduct :product="product" />
        </div>
      </div>


    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbb from '@/components/NavigationBar'
import HerBan from '@/components/HeroBanner'
import CardProduct from '@/components/CardProduct'
import axios from "axios"

export default {
  name: 'HomeView',
  components: {
    Navbb,
    HerBan,
    CardProduct
  },
  data() {
    return {
      products: []
    }
  },
  methods: {
    setProducts(data) {
      this.products = data
    }
  },
  mounted() {
    axios.get('http://localhost:3000/best-products')
      .then((response) => this.setProducts(response.data))
      .catch((error) => console.log(error))
  }
}
</script>
