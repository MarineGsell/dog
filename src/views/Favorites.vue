<template>
  <v-list>
    <v-subheader v-if="!favorites.length"
      >Your favorites list is empty</v-subheader
    >
    <div v-else>
      <v-subheader>Your favorites</v-subheader>
      <v-list-item v-for="(dog, index) in favorites" :key="index" @click="{}">
        <v-list-item-avatar>
          <img :src="dog.img" />
        </v-list-item-avatar>
        <v-list-item-content>{{dog.name}}</v-list-item-content>
        <v-list-item-action>
        <v-icon @click="$store.dispatch('removeFromFavorites', dog)">delete</v-icon>
        </v-list-item-action>
      </v-list-item>
      <div class="center">
        <v-btn to="/form">Adopt</v-btn>
      </div>
    </div>
  </v-list>
</template>

<script>
  export default {
    computed: {
      favorites() {
        return this.$store.state.favorites;
      }
    }
  };
</script>

<style>
.center {
  text-align: center;
}
</style>
