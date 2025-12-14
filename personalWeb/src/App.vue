<template>
  <div>
    <nav
      class="navbar navbar-expand-md bg-light"
      style="position: fixed; width: 100%"
    >
      <div class="navbar-brand"></div>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarToggleExternalContent"
        aria-controls="navbarToggleExternalContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div
        class="collapse navbar-collapse"
        id="navbarToggleExternalContent"
        style="justify-content: flex-end; margin: 0px 20px"
      >
        <ul class="navbar-nav mainFontSize">
          <li class="nav-item active">
            <router-link
              style="text-align: center"
              to="#PersonalInfo"
              class="nav-link mainFontColor navFont"
              >個人資料
            </router-link>
          </li>

          <li class="nav-item">
            <router-link
              class="nav-link mainFontColor navFont"
              to="#Portfolio"
              style="text-align: center"
              >作品集</router-link
            >
          </li>
          <li class="nav-item">
            <router-link
              class="nav-link mainFontColor navFont"
              to="#Autobiography"
              style="text-align: center"
              >簡歷</router-link
            >
          </li>
        </ul>
      </div>
    </nav>

    <RouterView ref="childComponent" />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },

  methods: {},
  mounted() {
    this.$router.afterEach((to, from) => {
      if (to.hash) {
        this.$nextTick(() => {
          const element = document.querySelector(to.hash);
          if (element) {
            element.scrollIntoView({ behavior: "smooth" });
          }
        });
      }
    });
  },
};
</script>

<style scoped>
.nav-link:focus,
.nav-link:hover {
  color: #528e81;
}
section {
  min-height: 700px;
  padding-top: 60px;
}
#section1,
#section4 {
  background-color: lightgray;
}
.navButton {
  padding: 0 !important;
  margin: 0 !important;
  background-color: transparent !important;
  border: 0;
  padding-top: 10px !important;
  font-size: 16px;
  color: #528e81;
}
.navbar {
  z-index: 100;
}
.v-enter-active,
.v-leave-active {
  transition: opacity 1s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
