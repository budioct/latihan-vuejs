<template>

  <div>
    <b-navbar toggleable="lg" type="light">
      <div class="container">
        <b-navbar-brand href="#">Kulineran</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <li class="nav-item">
              <router-link class="nav-link" to="/">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/foods">Foods</router-link>
            </li>
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <li class="nav-item">
              <router-link class="nav-link" to="/keranjang">
                Keranjang
                <b-icon-bag></b-icon-bag>
                <span class="badge badge-success ml-2">{{
                    updateKeranjang ? updateKeranjang.length : jumlah_pesanan.length
                  }}</span>
              </router-link>
            </li>
          </b-navbar-nav>
        </b-collapse>
      </div>

    </b-navbar>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "NavbarSite",
  data: function () {
    return {
      jumlah_pesanan: []
    }
  },
  props: ["updateKeranjang"],
  methods: {
    setJumlah(param) {
      this.jumlah_pesanan = param;
    }
  },
  mounted: function () {
    axios
        .get("http://localhost:3000/keranjangs")
        .then((response) => this.setJumlah(response.data))
        .catch((error) => console.info(error))
    // .then((response) => console.info(response))
  },
}
</script>

<style>

</style>