<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title font-weight-bold">Product Listing</h5>
      <b-table
        :fields="fields"
        :items="products"
        :sort-by.sync="sortBy"
        :sort-desc.sync="sortDesc"
        sort-icon-left
      >
        <template v-slot:cell(actions)="data">
          <input type="checkbox" />
        </template>
        <template v-slot:cell(status)="data">
          <div v-if="data.item.status" class="d-flex align-items-center">
            <span class="status status-green mr-2"></span> Activated
          </div>
          <div v-if="!data.item.status" class="d-flex align-items-center">
            <span class="status status-red mr-2"></span> Deactivated
          </div>
        </template>
      </b-table>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    products: [],
    sortBy: 'status',
    sortDesc: true,
    fields: [
      { key: 'actions', label: '' },
      { key: 'productName', label: 'Product Name' },
      { key: 'brandName', label: 'Brand Name' },
      { key: 'service', label: 'Service' },
      { key: 'status', label: 'Status' }
    ]
  }),

  async beforeMount() {
    const { data } = await this.$axios.get(
      `https://app.fakejson.com/q/35e4IEpQ?token=o6VoAJG8o_Oe7u8RWC9asQ`
    )

    this.products = data.products
  }
}
</script>

<style>
.status {
  width: 10px;
  height: 10px;
  border-radius: 100%;
}
.status-green {
  background-color: #b4e55c;
}
.status-red {
  background-color: #ff3b30;
}
</style>
