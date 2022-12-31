<!-- eslint-disable vue/valid-v-for -->
<template>
  <v-row>
    <v-col v-for="product in products" cols="2">
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
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 2,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 3,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 4,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 5,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 6,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 7,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 8,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 9,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 10,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 11,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 12,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 13,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 14,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
        {
          id: 15,
          title: 'Asuz Zenfone',
          thumbnail: 'asus-zenfone.png',
          price: 2000000,
          category: 1,
        },
      ],
    }
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
