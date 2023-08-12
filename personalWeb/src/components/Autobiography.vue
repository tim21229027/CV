<template>
  <div id="Autobiography" class="AutobiographyBody">
    <!-- 子子组件的内容 -->
    <div class="Title">簡歷</div>
    <div class="AutobiographySection">
      <div class="AutobiographyText">
        <p>「關於我」-</p>
        <p>
          畢業於中原大學訊管理系，名子是楊子瑨，覺得開發程式很有成就感，擅長前端開發與api串接，主要精通於Vue，個性隨和，大學除了課業專題上，也參加許多關於資訊管理的比賽，喜歡運動，大學為跆拳道校隊與副社長。
        </p>
        <p>「工作經歷」-</p>
        <p>
          曾任職於智弋科技股份有限公司擔任實習生，時長為一年半，主要負責項目為網頁前端開發，在此期間學到了Python、MongoDB、Css、Vue、JavaScript、WebSocket、視訊開發的應用。
        </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
};
</script>
<style scoped>
.AutobiographyBody {
  background-color: #528e81;
  min-height: 400px;
  padding: 20px;
}
.AutobiographySection {
  display: flex;
  padding: 30px;
  min-height: 400px;
}
.AutobiographyText {
  color: #fff;
  font-size: 18px;
  font-weight: 900;
}
.Title {
  display: flex;
  justify-content: flex-end;
  font-size: 24px;
  font-weight: 900;
  text-decoration: underline;
  color: #fff;
}
</style>