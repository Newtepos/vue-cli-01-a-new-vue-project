<template>
  <section>
    <h2>My frineds</h2>
    <ul>
      <friend-contact/>
      <friend-contact/>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      frineds: [
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
