<template>
  <li>
    <h2>{{ friend.name }}</h2>
    <button @click="toggleDetails">
      {{ detailsAreVisible ? "Hide Details" : "Show Details" }}
    </button>
    <ul v-if="detailsAreVisible">
      <li><strong>Phone:</strong>{{ friend.phone }}</li>
      <li><strong>Email:</strong>{{ friend.email }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  data() {
    return {
      detailsAreVisible: false,
      friend: { id: "1", name: "Inna", phone: "123456", email: "hi@gmail.com" },
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
  },
};
</script>

<style scoped></style>
