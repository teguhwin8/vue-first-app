<template>
  <li>
    <h2>{{ friend.name }}</h2>
    <button @click="toggleDetails()">Show Details</button>
    <ul :class="detailsAreVisible ? '' : 'd-none'">
      <li>
        <strong>Phone: {{ friend.phone }}</strong>
      </li>
      <li>
        <strong>Email: {{ friend.email }}</strong>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
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

<style>
.d-none {
  display: none;
}
</style>
