<template>
  <div>
    <button @click="switch_layout">Switch layout</button>
    <article>
      <h3>user: {{ user1 }}</h3>
      <p>content: {{ content1 }}</p>
      <h4>date created: {{ date_created1 }}</h4>
    </article>
    <article>
      <h3>user: {{ user2 }}</h3>
      <p>content: {{ content2 }}</p>
      <h4>date created: {{ date_created2 }}</h4>
    </article>
    <article>
      <h3>user: {{ user3 }}</h3>
      <p>content: {{ content3 }}</p>
      <h4>date created: {{ date_created3 }}</h4>
    </article>
    <article>
      <h3>user: {{ user4 }}</h3>
      <p>content: {{ content4 }}</p>
      <h4>date created: {{ date_created4 }}</h4>
    </article>
    <article>
      <h3>user: {{ user5 }}</h3>
      <p>content: {{ content5 }}</p>
      <h4>date created: {{ date_created5 }}</h4>
    </article>
  </div>
</template>

<script>
export default {
  methods: {
    switch_layout: function () {
      if (columns === 1) {
        this.colums = 3;
      } else {
        this.colums = 1;
      }
    },
  },
  //adding variables for the html to refer too
  data() {
    return {
      user1: `Dale`,
      content1: `lorem ipsum blah blah blah`,
      date_created1: `4 / 15 / 2023`,

      user2: `Dale1`,
      content2: `lorem ipsum blah blah blah`,
      date_created2: `4 / 15 / 2023`,

      user3: `Dale2`,
      content3: `lorem ipsum blah blah blah`,
      date_created3: `4 / 15 / 2023`,

      user4: `Dale3`,
      content4: `lorem ipsum blah blah blah`,
      date_created4: `4 / 15 / 2023`,

      user5: `Dale4`,
      content5: `lorem ipsum blah blah blah`,
      date_created5: `4 / 15 / 2023`,

      colums: 1,
    };
  },
};
</script>

<style scoped>
</style>