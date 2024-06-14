<script>
import _ from "lodash";
export default {
  data() {
    return {
      names: ["Neel", "Vasu", "Harsh"],
      movies: [
        {
          title: "Dilwale Dulhania Le Jayenge",
        },
        {
          title: "Sholay",
        },
        {
          title: "3 Idiots",
        },
        {
          title: "Dangal",
        },
        {
          title: "Kabhi Khushi Kabhie Gham",
        },
      ],
    };
  },
  methods: {
    shuffle() {
      console.log("Button is Press");
      this.names = _.shuffle(this.names);
    },
  },
};
</script>

<template>
  <div v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <input type="text" placeholder="Enter your Last Name" />
    <hr />
  </div>
  <button @click="shuffle">Shuffle</button>
  <div>
    <ul>
      <li v-for="movie in movies" :key="movie.title">
        {{ movie.title }}
      </li>
    </ul>
  </div>
</template>

<style></style>
