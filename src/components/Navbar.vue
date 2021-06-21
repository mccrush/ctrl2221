<template>
  <nav class="navbar navbar-expand-md navbar-light bg-light">
    <div class="container-fluid">
      <ul class="navbar-nav me-auto">
        <li class="nav-item">
          <router-link to="/" class="nav-link">Index</router-link>
        </li>
        <!-- <li class="nav-item">
          <router-link to="/razdel/page" class="nav-link">Page</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/razdel/about" class="nav-link">About</router-link>
        </li> -->
        <div class="dropdown">
          <a
            class="nav-link dropdown-toggle"
            href="#"
            role="button"
            id="dropdownMenuNapravs"
            data-bs-toggle="dropdown"
            aria-expanded="false"
          >
            Направления
          </a>

          <ul class="dropdown-menu" aria-labelledby="dropdownMenuNapravs">
            <li v-for="item in napravs" :key="item.id">
              <router-link :to="'/napravs/' + item.alias" class="nav-link">{{
                item.title
              }}</router-link>
            </li>
          </ul>
        </div>
        <li class="nav-item">
          <router-link to="/login" class="nav-link">Login</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/admin" class="nav-link">Admin</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/404" class="nav-link">404</router-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import { Dropdown } from 'bootstrap'
import napravs from '../data/napravs'
export default {
  // props: {
  //   napravs: {
  //     type: Array
  //   }
  // },
  data() {
    return {
      napravs
    }
  }
}
</script>