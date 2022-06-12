<template>
  <li>
    <header>
      <h1>{{ name }} {{ isFavorite === true ? "(Favorite)" : "" }}</h1>
    </header>
    <button @click="toggleFavorite">Toogle Favorite</button>
    <button @click="toggleDetails">Show Details</button>
    <button @click="this.$emit('delete', id)">Delete</button>
    <ul v-if="visibility">
      <li><strong>Phone: </strong>{{ phoneNumber }}</li>
      <li><strong>Email: </strong>{{ emailAddress }}</li>
    </ul>
  </li>
</template>

<script>
export default {
  // props: ["name", "phoneNumber", "emailAddress", "isFavorite"],
  props: {
    id: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    phoneNumber: {
      type: String,
      required: true,
    },
    emailAddress: {
      type: String,
      required: true,
    },
    isFavorite: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
  emits: ['toggle-favorite'],
  // emits: {
  //   'toggle-favorite': function(id) {
  //     if(id) {
  //       return true;
  //     } else {
  //       console.warn('Id is missing')
  //       return false;
  //     }
  //   }
  // },
  data() {
    return {
      visibility: false,
    };
  },
  methods: {
    toggleDetails() {
      this.visibility = !this.visibility;
    },
    toggleFavorite() {
      // this.friendIsFavorite = !this.friendIsFavorite;
      this.$emit('toggle-favorite', this.id);
    },
  },
};
</script>

