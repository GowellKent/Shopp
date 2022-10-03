<template>
  <div class="card mx-auto d-block" style="width: 18rem;">
    <img :src="'/assets/images/'+product.gambar" class="card-img-top" v-bind:alt="product.gambar" height="350px">
    <div class="card-body">
      <h5 class="card-title"><strong>{{product.nama}}</strong></h5>
      <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
        content.</p>
      <button class="btn btn-lg btn-primary">
        <b-icon-arrow-right></b-icon-arrow-right> Order
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardProduct',
  props: ['product']
}
</script>

<style>

</style>