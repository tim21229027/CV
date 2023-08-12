<template>
  <div class="skillCard">
    <div class="skillCardHeader">
      <div :style="skillTitleColor" class="skillTitleText">
        {{ skillTitle }}
      </div>
      <div class="skillTitleHr" :style="skillHrColor"></div>
    </div>
    <div class="skillCardBody">
      <el-scrollbar height="260px">
        <BasicInfo
          v-for="item in skillList"
          :key="item"
          :basicMainInfo="item.basicMainInfo"
          :markColor="item.markColor"
        ></BasicInfo>
      </el-scrollbar>
    </div>
  </div>
</template>
<script>
import BasicInfo from "@/components/basicInfo.vue";
export default {
  data() {
    return {};
  },
  props: {
    skillTitle: String,
    skillTitleColor: String,
    skillHrColor: String,
    skillList: Object,
  },
  components: {
    BasicInfo,
  },
  mounted() {},
};
</script>
<style scoped>
.skillCard {
  width: 320px;
  height: 340px;
  box-shadow: 1px 1px 10px 1px;
  margin: 20px;
  border-radius: 10px;
  background-color: #fff;
}
.skillTitleText {
  text-align: right;
  font-size: 18px;
  font-weight: 900;
  padding-right: 10px;
  padding-top: 20px;
}
.skillCardHeader {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  padding-right: 20px;
}
.skillTitleHr {
  height: 4px;

  border-radius: 30px;
  width: 100px;
}
.skillCardBody {
  margin-top: 10px;
}
</style>