<template>
  <!--<v-card color="grey lighten-2">
    <v-img :src="dog.img" height="170px"></v-img>
    <v-card-title>
      <div>
        <h3>{{dog.name}}</h3>
        <p class="breed">{{dog.breed}}</p>
      </div>
    </v-card-title>
    <v-btn @click="$emit('addToFavorites', dog)">Add to Favorites</v-btn>
  </v-card>-->

  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      :src="dog.img"
    >
      <v-card-title><h3>{{dog.name}}</h3></v-card-title>
    </v-img>

    <v-card-title>{{dog.breed}}</v-card-title>

    <v-card-text class="text--primary">
      <div>located : {{dog.location}}</div>

      <div>age : {{dog.age}}</div>
    </v-card-text>

    <v-card-actions align="center">
       <v-spacer></v-spacer>
      <v-btn
        color="pink"
       icon
      >
      <v-icon>favorite</v-icon>
      </v-btn>

   
       <v-spacer></v-spacer>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    dog: {
      type: Object
    }
  }
};
</script>
