<template>
  <div class="not-found">

    <div class="container">
      <div class="d-none d-md-block">
        <div class="row mt-4">
          <div class="col-md-6">
            <div class="d-flex h-100">
              <div class="justify-content-center align-self-center">
                <h2><strong>Not Found! - 404 </strong></h2>
                <router-link to="/" class="btn btn-lg btn-success">
                  <b-icon-house-door></b-icon-house-door>
                  Go home?
                </router-link>
              </div>
            </div>
          </div>
          <div class="col-md-6">
            <img :src="'../assets/images/back.png'" width="100%">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: "NotFound"
}

</script>

<style>

</style>