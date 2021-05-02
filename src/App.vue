<template>
  <section>
    <h2>My Friends</h2>
    <ul>
      <friend-contact></friend-contact>
      <friend-contact></friend-contact>
    </ul>
  </section>
</template>

<script>

export default {
  data() {
    return {
      friends: [
        {
          id: "teguh",
          name: "Teguh Widodo",
          phone: "085868474405",
          email: "teguhwin8@gmail.com",
        },
        {
          id: "fitri",
          name: "Fitriyani",
          phone: "085726575909",
          email: "fyani2288@gmail.com",
        },
      ],
    }
  },
}
</script>
