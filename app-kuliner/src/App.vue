<template>
  <div id="app">
    <router-view/>
    <FooterSite/>
  </div>
</template>

<script>
import FooterSite from "@/components/FooterSite.vue";

export default {
  components: {
    FooterSite
  }
}

</script>
