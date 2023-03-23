<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <nav class="navbar bg-body-tertiary fixed-top">
    <div class="container-fluid">
      <!-- <img class="navbar-brand" src="" /> -->

      <h6 class="navbar-brand">Pro</h6>

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="offcanvas"
        data-bs-target="#offcanvasNavbar"
        aria-controls="offcanvasNavbar"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div
        class="offcanvas offcanvas-end"
        tabindex="-1"
        id="offcanvasNavbar"
        aria-labelledby="offcanvasNavbarLabel"
      >
        <div class="offcanvas-header">
          <h5 class="offcanvas-title" id="offcanvasNavbarLabel">Pro</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="offcanvas"
            aria-label="Close"
          ></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
            <li class="nav-item">
              <RouterLink class="nav-link active" aria-current="page" to="/"
                >A</RouterLink
              >
            </li>

            <li class="nav-item">
              <RouterLink class="nav-link" to="/about">B</RouterLink>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
  <RouterView />
</template>

<style scoped>
.offcanvas-title {
  color: rgb(0, 0, 0);
}

.navbar-toggler {
  background: rgb(255, 255, 255);
}

.navbar-brand {
  height: 70px;
  width: 70px;
  border-radius: 50px;
}
</style>
