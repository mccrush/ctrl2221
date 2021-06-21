<template>
  <nav class="navbar navbar-expand-md navbar-light bg-light">
    <div class="container-fluid">
      <ul class="navbar-nav me-auto">
        <li class="nav-item">
          <router-link to="/" class="nav-link">Index</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/razdel" class="nav-link">Razdel</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/razdel/page" class="nav-link">Page</router-link>
        </li>
        <li class="nav-item">
          <router-link to="/razdel/about" class="nav-link">About</router-link>
        </li>
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