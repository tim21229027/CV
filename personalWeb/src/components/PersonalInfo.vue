<template>
  <div id="PersonalInfo" class="PersonalInfoBody">
    <div class="personalInfoHeader">
      <div class="personalInfoNameText personalUn">
        中原大學-資訊管理系-學士畢業
      </div>
      <div class="personalInfoHeaderLeft">
        <div class="personalInfoPhoto">
          <img src="@/assets/me.jpg" style="width: 100%" alt="personalPhoto" />
        </div>
        <div class="personalInfoName">
          <div class="personalInfoNameText">楊子瑨</div>
          <div class="personalInfoNameText">YANG,ZI-JIN</div>
        </div>

        <div class="personalInfoTag">
          <el-tag
            v-for="item in items"
            :key="item.label"
            :type="item.type"
            class="mx-1"
            effect="dark"
            round
            >{{ item.label }}</el-tag
          >
        </div>
      </div>
    </div>

    <div class="personalInformation">
      <div class="basicInfoBlock">
        <BasicInfo
          v-for="item in basicList"
          :key="item"
          :basicMainInfo="item.basicMainInfo"
          :basicSecondaryInfo="item.basicSecondaryInfo"
          :markColor="item.markColor"
        />
      </div>

      <div class="skillInfoBlock">
        <el-carousel type="card" height="400px" :autoplay="false">
          <el-carousel-item
            v-for="item in skillList"
            :key="item"
            justify="center"
          >
            <SkillCard
              :key="item"
              :skillList="item.basic"
              :skillTitle="item.title"
              :skillTitleColor="item.skillTitleColor"
              :skillHrColor="item.skillHrColor"
            />
          </el-carousel-item>
        </el-carousel>
      </div>
    </div>
  </div>
</template>
<script>
import BasicInfo from "@/components/basicInfo.vue";
import SkillCard from "@/components/skillCard.vue";
export default {
  data() {
    return {
      items: [
        { type: "info", label: "愛運動" },
        { type: "info", label: "熱愛思考" },
        { type: "info", label: "務實" },
      ],
      basicList: [
        {
          basicMainInfo: "E-mail",
          basicSecondaryInfo: "tt33252637@gmail.com",
          markColor: " background-color: #100B00;",
        },
        {
          basicMainInfo: "Phone Number",
          basicSecondaryInfo: "+886 0909919131",
          markColor: " background-color: #100B00;",
        },
        {
          basicMainInfo: "gitHub",
          basicSecondaryInfo: "tim21229027",
          markColor: " background-color: #100B00;",
        },
      ],
      skillList: [
        {
          title: "擅長程式",
          skillTitleColor: "color: #528E81;",
          skillHrColor: "background-color: #528E81;",
          basic: [
            {
              basicMainInfo: "HTML&CSS",
              markColor: " background-color: #528E81;",
            },
            {
              basicMainInfo: "JavaScript",
              markColor: " background-color: #528E81;",
            },
            {
              basicMainInfo: "Python",
              markColor: " background-color: #528E81;",
            },
            {
              basicMainInfo: "MySQL",
              markColor: " background-color: #528E81;",
            },
            {
              basicMainInfo: "Vue",
              markColor: " background-color: #528E81;",
            },
            {
              basicMainInfo: "MongoDB",
              markColor: " background-color: #528E81;",
            },
            {
              basicMainInfo: "FireBase",
              markColor: " background-color: #528E81;",
            },
          ],
        },

        {
          title: "開發經驗",
          skillTitleColor: "color: #6A52C2;",
          skillHrColor: "background-color: #6A52C2;",
          basic: [
            {
              basicMainInfo: "Vue.js網頁開發",
              markColor: " background-color: #6A52C2;",
            },

            {
              basicMainInfo: "API串接",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "webSocket",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "視訊及聊天室",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "LineBot",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "架設資料庫",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "JSP網頁開發",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "indexDB",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "UI/UX設計",
              markColor: " background-color: #6A52C2;",
            },
            {
              basicMainInfo: "系統流程設計",
              markColor: " background-color: #6A52C2;",
            },
          ],
        },

        {
          title: "個人經歷",
          skillTitleColor: "color: #B83624;",
          skillHrColor: "background-color: #B83624;",
          basic: [
            {
              basicMainInfo: "智弋科技前端實習工程師",
              markColor: " background-color: #B83624;",
            },
            {
              basicMainInfo: "InnoServe 2022 資訊應用組-冠軍",
              markColor: " background-color: #B83624;",
            },
            {
              basicMainInfo: "2022 Young Power 點子王創意競賽-季軍",
              markColor: " background-color: #B83624;",
            },
            {
              basicMainInfo: "2022桃園新創之星 X 創天下競賽-銅獎",
              markColor: " background-color: #B83624;",
            },
          ],
        },
      ],

      blackColor: " background-color: #100B00;",
    };
  },
  components: {
    BasicInfo,
    SkillCard,
  },
};
</script>
<style scoped>
.el-carousel__item:nth-child(2n) {
  display: flex;
  justify-content: center;
  overflow: initial;
  align-items: center;
}

.el-carousel__item:nth-child(2n + 1) {
  display: flex;
  justify-content: center;
  overflow: initial;
  align-items: center;
}
.skillInfoBlock /deep/ .el-carousel__button {
  background: #000 !important;
}
.PersonalInfoBody {
  padding-top: 60px;
  min-height: 700px;
}
.personalInfoHeader {
  background-color: #d9d9d9;
  text-align: right;
  padding: 10px;
}

.personalInfoHeaderLeft {
  display: flex;
}
.personalInfoName {
  font-size: 20px;
  text-align: left;
  margin-left: 40px;
}
.personalInfoNameText {
  font-weight: bold;
}
.personalInfoTag {
  padding-top: 32px;
  margin-left: 40px;
  text-align: left;
}

.personalUn {
  padding: 10px;
  font-size: 16px;

  margin-left: 40px;
}
.personalInformation {
  margin-top: 100px;
  display: flex;
  padding-left: 20px;
  padding-right: 20px;
}

@media screen and (max-width: 768px) {
  .personalInformation {
    margin-top: 20px;
    flex-wrap: wrap;
    justify-content: center;
  }
  .basicInfoBlock {
    flex-wrap: wrap;
  }
  .personalInfoPhoto {
    position: relative;
    width: 50px;
    height: 50px;
    border-radius: 100%;
    overflow: hidden;
    margin-left: 4%;
    display: flex;
    align-items: flex-start;
  }
  .personalInfoHeaderLeft {
    flex-wrap: wrap;
  }
  .personalInfoName {
    font-size: 16px;
    text-align: left;
    margin-left: 20px;
  }
  .personalInfoTag {
    padding-top: 12px;
    margin-left: 16px;
  }
  .personalUn {
    font-size: 12px;
  }
}
@media screen and (min-width: 769px) {
  .basicInfoBlock {
    padding-top: 50px;
    padding-left: 50px;
    width: 300px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .personalInfoPhoto {
    position: relative;
    width: 180px;
    height: 180px;
    border-radius: 100%;
    overflow: hidden;
    margin-left: 4%;
    display: flex;
    align-items: flex-start;
  }
  .personalInfoHeader {
    height: 140px;
    background-color: #d9d9d9;
    text-align: right;
  }
}

.skillInfoBlock {
  width: 100%;
}
.scrollbar-flex-content {
  display: flex;
}
</style>