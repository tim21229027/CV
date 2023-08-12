<template>
  <div class="basicInfoCard">
    <div><div class="basicMark" :style="markColor"></div></div>
    <div>
      <div class="basicMainText">{{ basicMainInfo }}</div>
      <div class="basicSecondaryText">{{ basicSecondaryInfo }}</div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
  props: {
    basicMainInfo: String,
    basicSecondaryInfo: String,
    markColor: String,
  },
};
</script>
<style scoped>
.basicMark {
  height: 20px;
  width: 20px;
  margin-right: 40px;
}
.basicInfoCard {
  display: flex;
  width: 280px;
  margin: 20px;
  align-items: center;
  justify-content: flex-start;
}

.basicMainText {
  font-size: 16px;
  font-weight: 600;
}
.basicSecondaryText {
  font-size: 16px;
  font-weight: 400;
}
</style>