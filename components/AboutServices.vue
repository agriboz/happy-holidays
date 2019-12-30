<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title font-weight-bold">About Services</h5>
      <div class="d-flex justify-content-between">
        <div
          :key="s.id"
          v-for="s in services"
          class="services-wrapper mt-3 d-flex"
        >
          <div class="services-item">
            <div class="services-body">
              <img
                :src="require(`@/assets/images/${s.imgSource}.png`)"
                :alt="s.title"
                class="position-absolute"
              />
              <div class="services-text position-absolute pl-2 pb-2">
                <h6 class="m-0 text-white">
                  <small>{{ s.title }}</small>
                </h6>
                <span class="text-white font-weight-bold"
                  >{{ s.currency.symbol }}{{ s.price }}</span
                >
              </div>
            </div>
            <div
              :style="{
                backgroundImage:
                  'url(' +
                  require('@/assets/images/' + `${s.descBg}` + '.png') +
                  ')'
              }"
              class="services-desc text-medium d-flex align-items-center justify-content-center text-white font-weight-bold mt-4"
            >
              {{ s.desc }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    services: [
      {
        id: 1,
        title: 'Carpenter',
        desc: 'Sofa Cleaning',
        descBg: 'services-sofa-cleaning',
        price: '45',
        imgSource: 'services-carpenter',
        currency: {
          name: 'Euro',
          symbol: '€',
          id: 1
        }
      },
      {
        id: 2,
        title: 'Ac Service & repair',
        desc: 'Bathroom Cleaning',
        descBg: 'services-bathroom-cleaning',
        price: '25',
        imgSource: 'services-ac',
        currency: {
          name: 'Euro',
          symbol: '€',
          id: 1
        }
      },
      {
        id: 3,
        title: 'Kitchen Deep Cleaning',
        desc: 'Pest Control',
        descBg: 'services-pest-control',
        price: '30',
        imgSource: 'services-kitchen',
        currency: {
          name: 'Euro',
          symbol: '€',
          id: 1
        }
      },
      {
        id: 4,
        title: 'Electrician',
        desc: 'View All',
        descBg: 'services-view-all',
        price: '50',
        imgSource: 'services-electirician',
        currency: {
          name: 'Euro',
          symbol: '€',
          id: 1
        }
      }
    ]
  })
}
</script>
