<template>
  <form @submit.prevent="submitData">
    <div>
      <label>Name</label>
      <input type="text" v-model="name" />
    </div>
    <div>
      <label>Phone</label>
      <input type="tel" v-model="phone" />
    </div>
    <div>
      <label>Email</label>
      <input type="email" v-model="email" />
    </div>
    <div>
      <button type="submit">Save</button>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      phone: '',
      email: ''
    }
  },
  methods: {
    submitData() {
      this.$emit (
        'add-contact',
        this.name,
        this.phone,
        this.email
      )
    }
  }
};
</script>

<style>
#app input {
  font: inherit;
  padding: 0.15rem;
}
#app label {
  font-weight: bold;
  margin-right: 1rem;
  width: 7rem;
  display: inline-block;
}
#app form div {
  margin: 1rem 0;
}
</style>