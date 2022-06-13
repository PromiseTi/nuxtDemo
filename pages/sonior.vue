<!--
* ----
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="padd-tb-ba text-center">
      <h1 class="margin-bottom-liu">{{ obj.hs1 }}</h1>
      <div class="lin-height-2 fontSize-14">
        <p>{{ obj.son1 }}</p>
        <p>{{ obj.son2 }}</p>
        <p class="margin-bottom-qi">{{ obj.son3 }}</p>
        <p>{{ obj.ss1 }}</p>
        <p>{{ obj.ss2 }}</p>
        <p>{{ obj.ss3 }}</p>
      </div>
    </div>
    <div class="sonsCont">
      <div class="widthSma flex flex-wrap marlrAuto">
        <div
          v-for="(item, index) in obj.list"
          :key="index"
          class="sonItem"
          :class="index % 2 == 0 && 'sonMar'"
        >
          <h2 class="margin-bottom">{{ item.a }}</h2>
          <div
            v-for="itemm in item.b"
            :key="itemm"
            class="lin-height-2 fontSize-14"
          >
            <p>{{ itemm }}</p>
          </div>
        </div>
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
        hs1: "What is Sonior?",
        son1: "Sonior is the name for SINSO contributors who share the vision and responsibility to make SINSO stronger and more valuable through",
        son2: "voluntary dedication in and out of the SINSO community.With great faith in Filecoin and the ecosystem, ",
        son3: "they recognize the idea and potentials of SINSO and are willing to bring added value and expand the popularity of the SINSO project.",
        ss1: "While blockchain has brought transformations to various industries, Filecoin, the worlds largest zero-knowledge proof network, ",
        ss2: "has rendered everyone more possibilities in the digital economy. As an important ecological partner of Protocol Labs,",
        ss3: "SINSO is the most advanced Layer 2 infrastructure architecture platform in the Filecoin ecosystem aiming to accelerate the development of the Metaverse.",
        list: [
          {
            a: "The Soniors We are Looking for...",
            b: [
              "Those with skills like programming, translation, content",
              "creation, design, community management, etc.",
              "Or can be a person who is a Web3.0 pioneer",
              "Or who is a wise sage",
              "Or a lone ranger with a unique belief",
              "Or who with a mission to inherit history and culture.",
            ],
          },
          {
            a: "How to Become a Sonior?",
            b: [
              "To join SINSO plus share the duties and well-being of a",
              "Sonior, you are expected to meet the requirements listed on",
              "the left  side and need to submit an application. SINSO will",
              "respond to your request within 7 days through email - please",
              "be patient and note your inbox messages.",
            ],
          },
          {
            a: "What Sonior Will Do?",
            b: [
              "The contributions you can make partly depend on your",
              "experience and the skills you have. What Soniors will",
              "do include technical work that constructs SINSO",
              "ecology and content creation to spread the deeds of",
              "SINSO and increase the visibility and influence of",
              "SINSO on a global scale.",
            ],
          },
          {
            a: "As a Sonior, You Can Get...",
            b: [
              "You can start your adventure in SINSO with your unique",
              "Sonior number,which as an honorary title will be used to",
              "record your growth in SINSOand receive exclusive bonuses.",
              "For other initiatives that you proposedand come to fruition,",
              "SINSO will also give equivalent rewards.",
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
.sonItem {
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
  width: 48%;
  height: 300px;
  margin-bottom: 50px;
  padding: 30px;
}
.sonMar {
  margin-right: 4%;
}
.sonsCont {
  background: linear-gradient(0deg, #d4eaf3 0%, rgba(255, 255, 255, 0) 100%);
  padding-bottom: 70px;
}
</style>
