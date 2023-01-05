<!-- eslint-disable vue/valid-v-for -->
<template>
  <v-row>
    <v-row>
      <v-col cols="10"> Search </v-col>
      <v-col cols="2">
        <v-menu>
          <template #activator="{ on: category }">
            <v-btn color="primary" v-on="category"> Category </v-btn>
          </template>

          <v-list>
            <v-list-item-group v-model="categoryId">
              <v-list-item
                v-for="(category, index) in categories"
                :key="index"
                :value="category.id"
              >
                <v-list-item-title>
                  {{ category.title }}
                </v-list-item-title>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-menu>
      </v-col>
    </v-row>

    <v-row>
      <v-col v-for="product in filteredProducts" cols="2">
        <v-card :key="product.id" :title="product.title" :ripple="true">
          <v-card-actions>
            <v-img
              :src="require(`@/assets/images/products/${product.thumbnail}`)"
            >
            </v-img>
          </v-card-actions>
          <v-card-text align="center" class="product-title">
            {{ product.title }}
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      categoryId: false,
      categories: [
        { id: false, title: 'All' },
        { id: 1, title: 'Smartphone' },
        { id: 2, title: 'Camera' },
        { id: 3, title: 'Televisi' },
      ],
      products: [
        {
          id: 1,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 2,
          title: 'Canon EOS 700D',
          thumbnail: 'canon-eos-700d.png',
          price: 2000000,
          categoryId: 2,
        },
        {
          id: 3,
          title: 'Canon EOS 750D',
          thumbnail: 'canon-eos-750d.png',
          price: 2000000,
          categoryId: 2,
        },
        {
          id: 4,
          title: 'Iphone 6 Silver',
          thumbnail: 'iphone-6-silver.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 5,
          title: 'Lenovo A7000',
          thumbnail: 'Lenovo-A7000.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 6,
          title: 'LG TV 32',
          thumbnail: 'lg-32-led-tv-32LF550A.png',
          price: 2000000,
          categoryId: 3,
        },
        {
          id: 7,
          title: 'LG TV 32',
          thumbnail: 'lg-led-tv32-32LF520A.png',
          price: 2000000,
          categoryId: 3,
        },
        {
          id: 8,
          title: 'Mi 4i',
          thumbnail: 'mi-4i.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 9,
          title: 'Nikon D3200',
          thumbnail: 'nikon-d3200.png',
          price: 2000000,
          categoryId: 2,
        },
        {
          id: 10,
          title: 'Nikon D5200',
          thumbnail: 'nikon-d5200.png',
          price: 2000000,
          categoryId: 2,
        },
        {
          id: 11,
          title: 'Samsung Galaxy A3',
          thumbnail: 'samsung-galaxy-A3.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 12,
          title: 'Samsung Galaxy A8',
          thumbnail: 'samsung-galaxy-A8.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 13,
          title: 'Samsung Galaxy Grand Prime',
          thumbnail: 'samsung-galaxy-grand-prime.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 14,
          title: 'Samsung Galaxy Note 3',
          thumbnail: 'samsung-galaxy-note-3.png',
          price: 2000000,
          categoryId: 1,
        },
        {
          id: 15,
          title: 'Sharp LED 32',
          thumbnail: 'sharp-32-led-32LE265i.png',
          price: 2000000,
          categoryId: 3,
        },
      ],
    }
  },
  // computed akan menjalankan setiap ada perubahan
  computed: {
    filteredProducts() {
      if (this.categoryId) {
        return this.products.filter((s) => s.categoryId === this.categoryId)
      }
      return this.products
    },
  },
}
</script>

<style>
.product-title {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
