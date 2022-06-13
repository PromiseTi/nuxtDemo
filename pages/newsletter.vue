<!--
* about newsletter h-
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="padd-tb-ba malrCont">
      <h1 class="margin-bottom-qi text-center wow fadeInUp">Newsletter</h1>
      <div
        class="margin-bottom-xl wow fadeInUp"
        v-for="(item, index) in list"
        :key="index"
      >
        <div class="docCont" :class="(item.f || item.g) && 'flexws'">
          <div class="">
            <h1 class="margin-bottom-xl">{{ item.a }}</h1>
            <div class="flex align-center">
              <p class="margin-right-sm letts">{{ item.b }}</p>
              <p class="fontSize-14 colo999">{{ item.c }}</p>
            </div>
            <p class="lin-height-2 margin-tb">
              {{ item.d }}
            </p>
            <p class="fontSize-14 colo999">{{ item.e }}</p>
          </div>
          <img v-if="item.f" :src="item.f" class="pcImg1" />

          <video
            v-if="item.g"
            src="https://bafybeihb3nvzbc6nlmlyeiynw24zx4qovexl274yhcdlbrb4yuo656uw54.ipfs.dweb.link/sinso1.mp4"
            controls="controls"
            class="pcImg1"
          >
            您的浏览器不支持 video 标签。
          </video>
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
      obj: [],
      list: [
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "In the first week after the Lunar New Year holidays, the development work of SINSO project is progressing steadily according to the product plan. At present, the number of accessed nodes to the test network is 6,748. After upgrading SINSO website’s UI interface, all SINSO development forces continued to focus on the...",
          e: "16 hours ago",
          f: "",
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "This week, SINSO development team continued speeding up the construction and deployment of the Testnet, and the current number of accessed nodes is 5,293. In addition, SINSO development team has carried out a new round of upgrades to the network background accelerator, and provided one-to-one assistance to solve the...",
          e: "16 hours ago",
          f: "",
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "This week, SINSO development team focused their efforts on the Testnet, to which the accessed nodes have topped 4000. SINSO development team streamlined and optimized the background...",
          e: "16 hours ago",
          f: require("../static/newsletter/pic.png"),
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "SINSO development team upgraded the Testnet seamlessly twice this week and added four basic control functions, solving the transmission inefficiency and error reporting problems raised by...",
          e: "16 hours ago",
          f: "",
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "This week, the R&D team continuously focused work on SINSO Distributed Cache Testnet. The current number of accessed nodes in Testnet has reached 1977. The R&D team has carried out...",
          e: "16 hours ago",
          f: "",
          g: "https://bafybeiavnxa6k76wjpjedljka52xlda4dlmyuwkhoeqe4uuxgbjrajwqau.ipfs.dweb.link/sinso1.mp4",
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "This week, SINSO R&D team continued to focus team work on SINSO Distributed Cache Testnet, whose current nodes have reached 1,360. SINSO team addressed problems like the...",
          e: "16 hours ago",
          f: "",
          g: "https://bafybeiavnxa6k76wjpjedljka52xlda4dlmyuwkhoeqe4uuxgbjrajwqau.ipfs.dweb.link/sinso2.mp4",
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "This week, SINSO continued to focus R&D work on the Distributed Cache Testnet, optimized deployment of the data ports through which some cache nodes connected to users, and prepared for the...",
          e: "16 hours ago",
          f: "",
          g: "https://bafybeiavnxa6k76wjpjedljka52xlda4dlmyuwkhoeqe4uuxgbjrajwqau.ipfs.dweb.link/sinso3.mp4",
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "The distributed-cache Testnet of SINSO is running smoothly. The R&D team’s major task for this week was to ensure successful access and debugging of whitelist node users. Apart from that, the...",
          e: "16 hours ago",
          f: "",
          g: "https://bafybeid3ukpgnqelfgauighee2ppypepj6vpo6cvqwn4mpfhebifomo2dm.ipfs.dweb.link/sinso4.mp4",
        },
        {
          a: "SINSO Weekly Newsletter",
          b: "Fliecoin",
          c: "2 min read",
          d: "The distributed-cache Testnet of SINSO is running smoothly. The R&D team’s major task for this week was to ensure successful access and debugging of whitelist node users. Apart from that, the...",
          e: "16 hours ago",
          f: "",
          g: "https://bafybeiavnxa6k76wjpjedljka52xlda4dlmyuwkhoeqe4uuxgbjrajwqau.ipfs.dweb.link/sinso5.mp4",
        },
      ],
    };
  },
  computed: {},
  methods: {
    // init() {
    //   let index = parseInt(this.$route?.query?.indexsssssss || 0);
    //   console.log(index);
    //   this.obj = this.$t("d.doDeta")[index];
    // },
  },
  created() {},
  mounted() {},
};
</script>
<style scoped>
.docCont {
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
  border-radius: 10px;
  padding: 30px;
  margin-bottom: 40px;
}
.fileImg {
  height: 80px;
}
.letts {
  padding: 8px 14px;
  background-color: #daf5ff;
  color: #00abeb;
  border-radius: 10px;
}
.pcImg1 {
  width: 440px;
  margin-left: 30px;
}
.flexws {
  display: flex;
  justify-content: space-between;
}
</style>
