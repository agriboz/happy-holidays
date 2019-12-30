<template>
  <div class="left-bar">
    <a
      href="#"
      class="menu-trigger d-flex justify-content-center align-items-center text-dark"
    >
      <font-awesome-icon far icon="chevron-left" />
    </a>
    <n-link to="/" class="d-flex align-items-center left-bar-brand-wrapper m-4">
      <div
        class="left-bar-brand d-flex align-items-center justify-content-center"
      >
        <img src="../assets/images/logo.png" alt="Technician" />
      </div>
      <div class="left-bar-brand-text d-flex flex-column mx-2">
        <span class="font-weight-bold text-large">Technician</span>
        <span>At Home</span>
      </div>
    </n-link>
    <ul class="navbar-nav mt-5">
      <li class="nav-item">
        <n-link class="nav-link active p-3" to="'dashboard'">
          <font-awesome-icon far icon="home" />
          <span class="ml-1">Dashboard</span>
        </n-link>
      </li>
      <li class="nav-item">
        <n-link class="nav-link p-3" to="'dashboard'">
          <font-awesome-icon far icon="cube" />
          <span class="ml-1">Product & Services</span>
        </n-link>
      </li>
      <li class="nav-item">
        <n-link class="nav-link p-3" to="'dashboard'">
          <font-awesome-icon far icon="user" />
          <span class="ml-1">Technicians</span>
        </n-link>
      </li>
      <li class="nav-item">
        <n-link class="nav-link p-3" to="'dashboard'">
          <font-awesome-icon far icon="calendar-alt" />
          <span class="ml-1">Reports</span>
        </n-link>
      </li>
      <li class="nav-item">
        <n-link class="nav-link p-3" to="'dashboard'">
          <font-awesome-icon far icon="comment-dots" />
          <span class="badge badge-info float-right">5</span>
          <span class="ml-1">Feedbacks</span>
        </n-link>
      </li>
      <li class="nav-item">
        <n-link class="nav-link p-3" to="'dashboard'">
          <font-awesome-icon far icon="history" />
          <span class="ml-1">History</span>
        </n-link>
      </li>
      <li class="nav-item">
        <n-link class="nav-link p-3" to="'dashboard'">
          <font-awesome-icon far icon="cog" />
          <span class="ml-1">Settings</span>
        </n-link>
      </li>
    </ul>
  </div>
</template>
