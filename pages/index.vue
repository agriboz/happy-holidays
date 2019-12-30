<template>
  <div class="content-page">
    <nav
      class="navbar navbar-expand navbar-light bg-white topbar mb-4 static-top"
    >
      <h3>Product & Services</h3>
      <!-- Topbar Navbar -->
      <ul class="navbar-nav ml-auto">
        <!-- Nav Item - User Information -->
        <li class="nav-item dropdown no-arrow">
          <a
            id="userDropdown"
            class="nav-link dropdown-toggle"
            href="#"
            role="button"
            data-toggle="dropdown"
            aria-haspopup="true"
            aria-expanded="false"
          >
            <img
              class="img-profile rounded-circle"
              src="../assets/images/avatar.png"
            />
            <span
              class="mr-2 d-none d-lg-inline text-gray-600 font-weight-bold small"
              >Belle</span
            >
          </a>
          <!-- Dropdown - User Information -->
          <div
            class="dropdown-menu dropdown-menu-right shadow animated--grow-in"
            aria-labelledby="userDropdown"
          >
            <a class="dropdown-item" href="#">
              <i class="fas fa-user fa-sm fa-fw mr-2 text-gray-400"></i>
              Profile
            </a>
            <a class="dropdown-item" href="#">
              <i class="fas fa-cogs fa-sm fa-fw mr-2 text-gray-400"></i>
              Settings
            </a>
            <a class="dropdown-item" href="#">
              <i class="fas fa-list fa-sm fa-fw mr-2 text-gray-400"></i>
              Activity Log
            </a>
            <div class="dropdown-divider"></div>
            <a
              class="dropdown-item"
              href="#"
              data-toggle="modal"
              data-target="#logoutModal"
            >
              <i class="fas fa-sign-out-alt fa-sm fa-fw mr-2 text-gray-400"></i>
              Logout
            </a>
          </div>
        </li>
      </ul>
    </nav>
    <div class="container-fluid">
      <div class="row">
        <div class="col-xl-8 col-lg-7">
          <about-services />
        </div>
        <div class="col-xl-4 col-lg-5">
          <add-technicians />
        </div>
      </div>
      <div class="row">
        <div class="col-xl-8 col-lg-7">
          <product-listing />
        </div>
        <div class="col-xl-4 col-lg-5"></div>
      </div>
    </div>
  </div>
</template>

<script>
import AboutServices from '@/components/AboutServices'
import AddTechnicians from '@/components/AddTechnicians'
import ProductListing from '@/components/ProductListing'

export default {
  components: {
    AboutServices,
    AddTechnicians,
    ProductListing
  }
}
</script>
