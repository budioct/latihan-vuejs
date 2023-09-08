<template>
  <div class="home">
    <NavbarSite/>
    <div class="container">
      <HeroSite/>

      <div class="row mt-4">
        <div class="col">
          <h2>Best <strong>Foods</strong></h2>
        </div>
        <div class="col">
          <router-link to="/foods" class="btn btn-success float-right">
            <b-icon-eye></b-icon-eye>
            Lihat Semua
          </router-link>
        </div>
      </div>

      <div class="row mb-4">
          <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
            <CardProductSite :product="product"/>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavbarSite from '@/components/NavbarSite.vue'
import HeroSite from '../components/HeroSite.vue'
import CardProductSite from "@/components/CardProductSite.vue";
import axios from "axios";

export default {
  name: 'HomeView',
  components: {
    NavbarSite,
    HeroSite,
    CardProductSite,
  },
  data: function () {
    return {
      products: []
    }
  },
  methods: {
    setProducts(param) {
      this.products = param;
    }
  },
  mounted: function () {
    axios
        .get("http://localhost:3000/best-products")
        .then((response) => this.setProducts(response.data))
        .catch((error) => console.info(error))
    // .then((response) => console.info(response))
  },
}
</script>
