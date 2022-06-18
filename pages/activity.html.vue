<!--
* ----
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <img style="width: 100%" src="/ecoPartner/acts.jpg" />
    <h1 class="padd-tb-ba text-center coloBls wow fadeInUp">{{ this.hh }}</h1>
    <div class="news-content">
      <div class="margin-bottom fontSize-20 wow fadeInUp">{{ act1.a }}</div>
      <div
        v-for="item in act1.b"
        :key="item"
        class="margin-bottom-xs wow fadeInUp"
      >
        {{ item }}
      </div>
      <div class="margin-tb fontSize-20 wow fadeInUp">{{ act2.a }}</div>
      <ul>
        <li
          v-for="item in act2.b"
          :key="item"
          class="margin-bottom-xs wow fadeInUp"
        >
          {{ item }}
        </li>
      </ul>
      <div class="margin-tb fontSize-20 wow fadeInUp">{{ act3.a }}</div>
      <div class="wow fadeInUp">{{ act3.b }}</div>
      <div class="margin-tb fontSize-20 wow fadeInUp">{{ act4.a }}</div>
      <div class="wow fadeInUp">{{ act4.b }}</div>
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
      hh: "Upcoming Events",
      act1: {
        a: "1. About this event:",
        b: [
          "Filecoin Singapore Summit (Filecoin-Empowering A Web3 World)",
          "SINSO is organizing a group (led by Franklin Jiang, Community Technical Leader) to Singapore on 17 August to meet various Web3 projects, financial institutions, as well as leaders from incredible communities across the country. We will unite to celebrate our progress in building Filecoin ecosystem. We are proudly supported by Protocol Labs & Filecoin Foundation.",
          "The event features engaging four days of panel discussions from Filecoin ecological participants, Web3 co-builders, top international speakers, and opportunities to connect and network with peers across diverse sectors.",
          "Start your summer right by joining us at Filecoin Singapore Summit.",
        ],
      },
      act2: {
        a: "2. What is covered in the event:",
        b: [
          "Case study of SINSO products;",
          "A networking event with venture capital firms & other financial institutions (more details to follow);",
          "Additional networking events with various project parties and web3 enthusiasts (more details to follow);",
          "Panel discussion ( Decentralized Hot Data Cache & Data Governance);",
          "On-site activities (Draw & AMA…);",
          "…",
        ],
      },
      act3: {
        a: "3. Date and time:",
        b: "Wed, 17 Aug 2022, 10:00 AM – 4:00 PM",
      },
      act4: {
        a: "4. Location::",
        b: "Singapore",
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
.news-content {
  padding: 0 360px;
  margin-bottom: 70px;
}
ul {
  margin-left: 20px;
}
li {
  list-style: disc;
}
@media screen and (max-width: 600px) {
  .news-content {
    padding: 0px 20px;
    margin-bottom: 30px;
  }
  .padd-tb-ba {
    padding: 40px 0px;
  }
}
</style>
