<template>
  <section>
    <h2>My frineds</h2>
    <ul>
      <friend-contact
        name="supakit pavaputanon"
        phone-number="063 020 0081"
        email-address="supakit.pnm@gmail.com"
        is-favorite="1"
      />
      <friend-contact
        name="thipsukol kobprasertsri"
        phone-number="081 753 2754"
        email-address="thipsukol@gmail.com"
        is-favorite="0"
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
