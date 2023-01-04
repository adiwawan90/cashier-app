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
            <v-list-item-group>
              <v-list-item v-for="(category, index) in categories" :key="index">
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
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      categories: [
        { id: 1, title: 'Smartphone' },
        { id: 2, title: 'Camera' },
        { id: 1, title: 'Televisi' },
      ],
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
