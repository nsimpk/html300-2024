<script setup>
import { ref } from 'vue'

const name = ref('Grid')
</script>

<template>
  <h1>GRID</h1>
  <div class="container">
              <div class="container">
                <div class="row">
                  <div class="col-xl-6 col-lg-5 col-md-4 col-sm-3 col-12 bg-warning">
                    1 of 3
                  </div>
                  <div class="col-xl-5 col-lg-5 col-md-4 col-sm-3 col-12 bg-info">
                    2 of 3
                  </div>
                  <div class="col-xl-1 col-lg-2 col-md-4 col-sm-6 col-12 bg-dark text-light">
                    3 of 3
                  </div>
                </div>
                <div class="row">
                  <div class="col-xl-5 col-lg-5 col-md-4 col-sm-3 col-12 bg-success">
                    1 of 3
                  </div>
                  <div class="col-xl-1 col-lg-2 col-md-4 col-sm-6 col-12 bg-dark text-light">
                    2 of 3
                  </div>
                  <div class="col-xl-6 col-lg-5 col-md-4 col-sm-3 col-12 bg-secondary">
                    3 of 3
                  </div>
                </div>
              </div>
            </div>
</template>

<style scoped>
.grid {
  text-align: center;
  margin-top: auto;
}
</style>
