<template>
  <div class="home">
    <Navbb />
    <div class="container">
      <HerBan />
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
          <CardProduct :product="product"/>
        </div>
        <div class="col-md-4 mt-4">
          <h2>item2</h2>
        </div>
        <div class="col-md-4 mt-4">
          <h2>itme3</h2>
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
    setProduct(data) {
      this.products = data
    }
  },
  mounted() {
    axios.get('http://localhost:3000/best-products')
      .then(function (response) {
        // handle success
        this.setProduct(response.data)
      })
      .catch(function (error) {
        // handle error
        console.log("Gagal ", error);
      })
  }
}
</script>
