<template>
  <div>
    <h1>Job Details Page</h1>
    <p>The job id is {{ id }}</p>
  </div>
</template>

<script>
export default {
  // add props: true in index
  props: ["id"],
  //   data() {
  //     return {
  //       id: this.$route.params.id,
  //     };
  //   },
};
</script>

<style></style>
