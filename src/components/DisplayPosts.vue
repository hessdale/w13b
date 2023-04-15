<template>
  <div>
    <article>
      <h3>user: {{ user }}</h3>
      <p>content: {{ content }}</p>
      <h4>date created: {{ date_created }}</h4>
    </article>
  </div>
</template>

<script>
export default {
  //adding variables for the html to refer too
  data() {
    return {
      user: `Dale`,
      content: `lorem ipsum blah blah blah`,
      date_created: `4 / 15 / 2023`,
    };
  },
};
</script>

<style scoped>
</style>