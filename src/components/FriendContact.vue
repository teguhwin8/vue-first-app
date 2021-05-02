<template>
  <li>
    <h2>{{ name }} {{ friendIsFavorite === '1' ? '(Favorite)' : '' }}</h2>
    <button @click="toggleFavorite()">Toggle Favorite</button>
    <button @click="toggleDetails()">{{ detailsAreVisible ? 'Hide' : 'Show' }} Details</button>
    <ul v-if="detailsAreVisible">
      <li>
        <strong>Phone: {{ phoneNumber }}</strong>
      </li>
      <li>
        <strong>Email: {{ emailAddress }}</strong>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  props: [
    'name',
    'phoneNumber',
    'emailAddress',
    'isFavorite'
  ],
  data() {
    return {
      detailsAreVisible: false,
      friend: {
        id: "teguh",
        name: "Teguh Widodo",
        phone: "085868474405",
        email: "teguhwin8@gmail.com",
      },
      friendIsFavorite: this.isFavorite
    }
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible
    },
    toggleFavorite() {
      if (this.friendIsFavorite === '1') {
        this.friendIsFavorite = '0'
      } else {
        this.friendIsFavorite = '1'
      }
    }
  },
}
</script>
