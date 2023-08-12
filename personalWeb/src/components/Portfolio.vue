<template>
  <div id="Portfolio" class="PortfolioBody">
    <!-- 子子组件的内容 -->
    <div class="Title">作品集</div>
    <div class="CardList">
      <div class="PortfolioCard" v-for="item in PortfolioList" :key="item">
        <div class="PortfolioPhoto">
          <img class="PortfolioImg" :src="item.PortfolioPhoto" />
        </div>
        <div class="PortfolioTitle">{{ item.PortfolioTitle }}</div>
        <div class="PortfolioItemText">負責項目:</div>
        <div class="PortfolioTag">
          <el-tag
            v-for="tags in item.PortfolioTag"
            :key="tags"
            class="mx-1"
            effect="dark"
            type="info"
            round
            >{{ tags }}</el-tag
          >
        </div>
        <div class="PortfolioItemText">開發使用工具:</div>
        <div class="PortfolioTag">
          <el-tag
            v-for="tags in item.PortfolioToolTag"
            :key="tags"
            class="mx-1"
            effect="dark"
            type="info"
            round
            >{{ tags }}</el-tag
          >
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import u1 from "@/assets/u1.png";
import u2 from "@/assets/u2.png";
import u3 from "@/assets/u3.png";
import u4 from "@/assets/u4.jpg";
import u5 from "@/assets/u5.png";
import u6 from "@/assets/u6.png";
export default {
  data() {
    return {
      PortfolioList: [
        {
          PortfolioPhoto: u1,
          PortfolioTitle: "大學畢業專題-INoteYou",
          PortfolioTag: [
            "前端設計",
            "UI/UX設計",
            "api串接",
            "系統流程規劃",
            "視訊開發",
          ],
          PortfolioToolTag: [
            "Vue",
            "agora",
            "Figma",
            "axios",
            "NaiveUI",
            "GitLab",
          ],
        },
        {
          PortfolioPhoto: u5,
          PortfolioTitle: "大三SA專題-疫調系統",
          PortfolioTag: ["前端設計", "UI/UX設計", "資料庫串接", "系統流程規劃"],
          PortfolioToolTag: ["Vue", "FireBase", "Figma"],
        },
        {
          PortfolioPhoto: u2,
          PortfolioTitle: "大二前端專題-電商",
          PortfolioTag: ["前端設計", "UI/UX設計"],
          PortfolioToolTag: ["Bootstrap"],
        },
        {
          PortfolioPhoto: u4,
          PortfolioTitle: "大二多媒體課程-社團",
          PortfolioTag: ["前端設計"],
          PortfolioToolTag: ["Bootstrap"],
        },
        {
          PortfolioPhoto: u3,
          PortfolioTitle: "大二後端專題-電商",
          PortfolioTag: ["資料庫架設", "前後端串接"],
          PortfolioToolTag: ["MySQL", "TomCat"],
        },
        {
          PortfolioPhoto: u6,
          PortfolioTitle: "LineBot-聊天機器人",
          PortfolioTag: ["聊天機器人開發", "Line圖文版面設計"],
          PortfolioToolTag: ["LINE Bot Designer", "Django"],
        },
      ],
    };
  },
};
</script>
<style scoped>
.PortfolioBody {
  min-height: 800px;
  padding: 20px;
}
.Title {
  display: flex;
  justify-content: flex-end;
  font-size: 24px;
  font-weight: 900;
  text-decoration: underline;
}
.CardList {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.PortfolioCard {
  height: 400px;
  width: 280px;
  box-shadow: gray 1px 1px 10px;
  border-radius: 8px;
  margin: 10px;
}
.PortfolioTitle {
  margin-top: 20px;
  font-size: 20px;
  font-weight: 600;
  text-align: center;
}
.PortfolioPhoto {
  height: 150px;
  width: 100%;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  border-bottom: 2px rgba(128, 128, 128, 0.323) solid;
  border-radius: 8px 8px 0px 0px;
}
.PortfolioItemText {
  margin: 8px 8px;
  font-weight: 600;
}
.PortfolioImg {
  width: 100%;
}
</style>