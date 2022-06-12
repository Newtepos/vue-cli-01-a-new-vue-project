<template>
  <section>
    <h2>My frineds</h2>
    <ul>
      <friend-contact
        v-for="friend in friends"
        :key="friend.id"
        :name="friend.name"
        :phone-number="friend.phone"
        :email-address="friend.email"
        :is-favorite="true"
      />
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      friends: [
        {
          id: "supakit",
          name: "supakit pavaputanon",
          phone: "063 020 0081",
          email: "supakit.pnm@gmail.com",
        },
        {
          id: "cheese",
          name: "thipsukol kobprasertsri",
          phone: "081 753 2754",
          email: "thipsukol@gmail.com",
        },
      ],
    };
  },
};
</script>
