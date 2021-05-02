<template>
  <li>
    <h2>{{ name }}</h2>
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
    'emailAddress'
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
    }
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible
    },
  },
}
</script>
