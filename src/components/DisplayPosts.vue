<template>
  <div>
    <!-- adding event lister with @click that uses a function to switch layout -->
    <button @click="switch_layout">Switch layout</button>
    <!-- a ref to change the column -->
    <div ref="column_setting">
      <!-- using a foor loop to inject the tweets -->
      <article v-for="(tweet, i) in tweets" :key="i">
        <h3>user: {{ tweet[`user`] }}</h3>
        <p>content: {{ tweet[`content`] }}</p>
        <h4>date created: {{ tweet[`date_created`] }}</h4>
      </article>
    </div>
  </div>
</template>

<script>
export default {
  //setting inline style back and forth comlumn and rows with attributes
  methods: {
    switch_layout: function () {
      if (this.$refs[`column_setting`][`style`][`gridAutoFlow`] !== `column`) {
        this.$refs[`column_setting`][`style`][`gridAutoFlow`] = `column`;
      } else {
        this.$refs[`column_setting`][`style`][`gridAutoFlow`] = `row`;
      }
    },
  },

  //adding variables for the html to refer too
  data() {
    return {
      tweets: [
        {
          user: `Dale`,
          content: `lorem ipsum blah blah blah`,
          date_created: `4 / 15 / 2023`,
        },

        {
          user: `Dale1`,
          content: `lorem ipsum blah blah blah`,
          date_created: `4 / 16 / 2023`,
        },

        {
          user: `Dale2`,
          content: `lorem ipsum blah blah blah`,
          date_created: `4 / 18 / 2023`,
        },

        {
          user: `Dale3`,
          content: `lorem ipsum blah blah blah`,
          date_created: `4 / 10 / 2023`,
        },

        {
          user: `Dale4`,
          content: `lorem ipsum blah blah blah`,
          date_created: `4 / 11 / 2023`,
        },
      ],
    };
  },
};
</script>

<style scoped>
div {
  display: grid;
}
button {
  width: 200px;
}
</style>