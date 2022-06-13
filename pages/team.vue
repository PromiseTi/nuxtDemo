<!--
* ----
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="padd-tb-ba teams">
      <h1 class="margin-bottom-liu">{{ obj.a }}</h1>
      <div class="lin-height-2 fontSize-14">
        <p>{{ obj.b1 }}</p>
        <p>{{ obj.b2 }}</p>
        <p>{{ obj.b3 }}</p>
        <p>{{ obj.b4 }}</p>
        <p>{{ obj.b5 }}</p>
        <p>{{ obj.b6 }}</p>
      </div>
    </div>
    <div class="backF3f5 padd-tb-ba">
      <div class="malrCont teaItem">
        <client-only>
          <el-carousel
            trigger="click"
            :interval="500000"
            arrow="always"
            height="500px"
          >
            <el-carousel-item
              v-for="(item, index) in obj.teamList"
              :key="index"
            >
              <div class="flex align-center justify-center teamKuang">
                <div class="text-center flexfrow padding-top-xl teaBlok">
                  <img class="teamPh" :src="'/team/team' + index + '.png'" />
                  <h3 class="margin-tb-sm">{{ item.hh1 }}</h3>
                  <p>{{ item.hh2 }}</p>
                </div>
                <div class="teaWid">
                  <div
                    v-for="itemm in item.itList"
                    :key="itemm"
                    class="lin-height-18"
                  >
                    <img src="/zhuangshi.png" class="kenPos" />
                    <p>{{ itemm }}</p>
                  </div>
                </div>
              </div>
            </el-carousel-item>
          </el-carousel>
        </client-only>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
  components: {},
  props: {},
  data() {
    return {
      obj: {
        a: "About Us",
        b1: "SINSO, as a Filecoin Layer2 and infrastructure of Web3.0 Ecosystem",
        b2: "will go online as Filecoin s first Layer2 network",
        b3: "With top technical team members from all over the world",
        b4: "SINSO draws support from the up-to-date achievements of the Filecoin network and expands the middle layer of Web3.0",
        b5: "By solving the application iteration and migratio problems caused by Filecoin’s lack of a complete ecological infrastructure system",
        b6: "SINSO propels the transition of a wide range of DAPPs from Web2.0 to Web3.0.",
        teamList: [
          {
            hh1: "Babar Mazher Khan",
            hh2: "CEO",
            itList: [
              "MBA in Finance degree from IBA;",
              "Post Graduate Diploma in Business Administration;",
              "As a Corporate Finance Manager, he was involved in many financing transactions from USD 150M to USD  3.5B dualtranche bonds issue, which was oversubscribed 7 times.",
            ],
          },
          {
            hh1: "Michael Karin",
            hh2: "CMS",
            itList: [
              "Fellow of the National Academy of Sciences;",
              "American National Research Expert Immunology",
              "Fellow of the American Association for Cancer Research;",
              "Fellow of the European Molecular Biology Society (EMBO).",
            ],
          },
          {
            hh1: "Michael Karin",
            hh2: "CFO&CRO",
            itList: [
              "25 years+ of diversified international banking & investment management experience;",
              "Fellow of the Association for the Advancement of Artificial Intelligence(AAAl);",
              "Fellow of the CFA Institute of Risk Professionals (USA).",
            ],
          },
          {
            hh1: "Franklin Jiang",
            hh2: "CTO",
            itList: [
              "15 years+ of medical  IT experience;",
              "Founder of China's earliest medical research and development team of Ethereum",
              "IPFS distributed storage application expert",
              "Initiator of the Global Web3 Medical Foundation.",
            ],
          },
          {
            hh1: "Mariya Ebirayim",
            hh2: "CBO",
            itList: [
              "9 years of experience in fintech investment field;",
              "6+ years of experiences in Business development, Branding & Digital marketing;",
              "Focused on the blockchain and fintech field.",
            ],
          },
        ],
      },
    };
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style scoped>
.teams {
  height: 500px;
  background: url("/team/teamBack.png") no-repeat;
  background-size: cover;
  text-align: center;
  color: #ffffff;
}
.teaItem {
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
}
.teaBlok {
  width: 400px;
  height: 300px;
  border-radius: 10px;
  background-color: #ffffff;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
  margin-right: 40px;
}
.teamKuang {
  height: 500px;
}
.teamPh {
  height: 100px;
  border-radius: 50%;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
}
.teaWid {
  width: 500px;
}
.teaWid > div {
  position: relative;
  padding-left: 30px;
}
.kenPos {
  position: absolute;
  left: 0;
  top: 8px;
  width: 15px;
}
</style>
