<template>
<div>
  <div class="pesanan-sukses">
    <NavbarSite />
    <div class="container">
      <div class="row justify-content-center mt-5">
        <div class="col text-center">
          <img :src="'../assets/images/menunggu.png'" width="300" />
          <h2><strong>Sukses!!</strong></h2>
          <h4>Pesanan Anda segera diproses <br> Selamat Menunggu</h4>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import NavbarSite from "@/components/NavbarSite.vue";

export default {
  name: "PesananSuksesView",
  components: {
    NavbarSite,
  },
}
</script>

<style>

</style>