<template>
  <main id="main">
    <div id="header">
      <Header />
    </div>
    <div id="form">
      <FormForm />
    </div>
  </main>
</template>

<script>
import Header from "@/components/HeaderForm.vue";
import FormForm from "@/components/FormForm.vue";

export default {
  name: 'HomeView',
  components: {
    Header,
    FormForm,
  }
}
</script>

<style scoped>
#header {
  height: 5vh;
}

#contents {
  height: 95vh;
}
</style>