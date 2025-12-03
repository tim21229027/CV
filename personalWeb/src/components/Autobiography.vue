<template>
  <div id="Autobiography" class="AutobiographyBody">
    <!-- 子子组件的内容 -->
    <div class="Title">簡歷</div>
    <div class="AutobiographySection">
      <div class="AutobiographyText">
        <p>「關於我」-</p>
        <p>
          畢業於中原大學資訊管理學系碩士班，個性穩重，喜歡透過技術解決實際問題。在學期間於智弋科技實習三年多，參與塑膠射出成型計算平台的開發與整合。前兩年主要負責前端開發，使用
          Vue.js + Element Plus 進行頁面設計、API
          串接與表單驗證，後期轉為前後端整合開發，負責API設計、應用與 Docker
          環境部署。透過這段經驗，我熟悉了完整的系統開發流程，能獨立完成專案規劃、開發與上線部署。
        </p>
        <p>「求學經歷」-</p>
        <p>
          我選擇資訊管理的原因，是因為寫出能解決問題的程式讓我感到成就感，而資管結合了程式設計、系統分析與專案管理，讓我學會從全局思考問題並設計具體解決方案。大學期間，我發現自己在多媒體開發與系統分析上特別有興趣，因此積極參與競賽與專題研究。
        </p>
        <p>
          在 2022
          年全國資訊管理專題競賽中，我與團隊開發「共同筆記整合系統」，透過自動摘要與關鍵字產生技術，協助師生快速掌握課程重點，最終榮獲一般組冠軍。在專題過程中，我負責
          以 Vue.js 進行前端介面開發，並結合課堂所學的
          系統分析與多媒體應用，設計整體 UI/UX 介面，完成 API
          串接與互動邏輯實作，專案期間多次與團隊溝通討論系統優化方向，培養了我在
          專案規劃、協作與問題解決上的能力。
        </p>
        <p>
          碩士期間參與台電能源負載預測計畫案，為期9個月，負責模型改善、資料處理，過程中學習到了如何使用
          Python、TensorFlow透過BiLSTM與LSTM模型幫助台電進行預測，同時以「應用XAI技術於
          DNS 資料外洩攻擊檢測模型」為碩士論文主題，探討如何利用 SHAP
          技術解析模型判斷邏輯並提升模型透明度。研究入選 2025
          崇越論文大賞決賽，讓我在 AI
          模型開發與資料分析方面累積了深厚的研究與實務經驗。
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