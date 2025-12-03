<script>
import PersonalInfo from "@/components/PersonalInfo.vue";
import Autobiography from "@/components/Autobiography.vue";
import Portfolio from "@/components/Portfolio.vue";
export default {
  data() {
    return {};
  },
  components: {
    PersonalInfo,
    Autobiography,
    Portfolio,
  },
};
</script>
<template>
  <div class="container">
    <div ref="myChildComponent" style="background-color: #f8f8f8">
      <section>
        <PersonalInfo />
      </section>

      <section><Portfolio /></section>
      <section>
        <Autobiography />
      </section>
    </div>
  </div>
</template>
<style scoped>
</style>