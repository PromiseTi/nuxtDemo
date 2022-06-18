<!--
* Heard
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div class="container">
    <header>
      <div class="flex jusstify-between align-center malrCont pc">
        <div class="flex align-center">
          <img class="logoImg" src="../static/logo.png" />
          <client-only>
            <NuxtLink
              type="text"
              v-for="(item, index) in heads"
              :key="index"
              class="fontsix"
              :class="[
                'fontS' + index,
                item.rot.includes($route.path) ? 'coloBls' : '',
              ]"
              :to="
                localePath({
                  name: item.name,
                })
              "
            >
              {{ item.t1 }}
              <!-- <a :class="item.rot.includes($route.path) && 'coloBls'"></a> -->
              <!-- <div class="menu-nav-first-ab about3">
                <NuxtLink :to="localePath({ name: 'ecoPartnerDetail' })"
                  >Filecoin动态</NuxtLink
                >
                <NuxtLink :to="localePath({ name: 'ecoPartner' })"
                  >Ecosystem Partners</NuxtLink
                >
              </div> -->
              <div class="menu-nav-first-ab about4">
                <NuxtLink :to="localePath({ name: 'dac' })"
                  >Introduction</NuxtLink
                >
                <NuxtLink :to="localePath({ name: 'member' })"
                  >Ambassador Program</NuxtLink
                >
                <NuxtLink :to="localePath({ name: 'sonior' })">Sonior</NuxtLink>
              </div>
              <div class="menu-nav-first-ab about6">
                <NuxtLink to="news">News & Updates</NuxtLink>
                <NuxtLink to="newsletter">NewsLetter</NuxtLink>
                <NuxtLink to="team">Team</NuxtLink>
              </div>
            </NuxtLink>
            <a class="fontsix" href="https://testnet.whitelist.vip/">{{
              $t("had.li8")
            }}</a>
          </client-only>
        </div>
        <div></div>
      </div>
      <div class="mob_Head">
        <img style="height: 40px" src="../static/logo.png" />
        <img
          @click.stop="isFlag = true"
          style="width: 30px"
          src="/mobile/index/gengduo.png"
        />
        <!--移动端导航菜单-->
        <div class="moblie-nav-wrap" :class="isFlag && 'showAp'">
          <div class="modal-layer-1 modal-layer-closed"></div>
          <div class="modal-layer-2">
            <img @click.stop="isFlag = false" src="/mobile/index/close.png" />
          </div>
          <div class="modal-layer-3">
            <ul>
              <li v-for="(item, index) in heads" :key="index">
                <NuxtLink
                  v-if="![4, 6].includes(index)"
                  :class="[item.rot.includes($route.path) ? 'coloBls' : '']"
                  :to="
                    localePath({
                      name: item.name,
                    })
                  "
                  >{{ item.t1 }}</NuxtLink
                >
                <a
                  v-else
                  :class="[
                    item.rot.includes($route.path) ? 'coloBls' : '',
                    [4, 6].includes(index) ? 'moblie-select' : '',
                    choIndex === index ? 'selectShow' : '',
                  ]"
                  @click="goTo(index)"
                  >{{ item.t1 }}</a
                >
                <div
                  class="moblie-select-list"
                  :class="choIndex == 4 && index == 4 && 'selectList'"
                >
                  <NuxtLink :to="localePath({ name: 'dac' })"
                    >Introduction</NuxtLink
                  >
                  <NuxtLink :to="localePath({ name: 'member' })"
                    >Ambassador Program</NuxtLink
                  >
                  <NuxtLink :to="localePath({ name: 'sonior' })"
                    >Sonior</NuxtLink
                  >
                </div>
                <div
                  class="moblie-select-list"
                  :class="choIndex == 6 && index == 6 && 'selectList'"
                >
                  <NuxtLink to="news">News & Updates</NuxtLink>
                  <NuxtLink to="newsletter">NewsLetter</NuxtLink>
                  <NuxtLink to="team">Team</NuxtLink>
                </div>
              </li>
              <!-- <li><a class="a-link" href="javascript:;">职池工作</a></li>
              <li>
                <a
                  class="moblie-select"
                  :class="choIndex == 1 && 'selectShow'"
                  @click="goJi(1)"
                  >宝航资讯</a
                >
                <div
                  class="moblie-select-list"
                  :class="choIndex == 1 && 'selectList'"
                >
                  <a href="news.html?index=0">行业前沿</a>
                  <a href="news.html?index=1">企业新闻</a>
                  <a href="news.html?index=2">企业追踪</a>
                </div>
              </li> -->
            </ul>
          </div>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "",
  components: {},
  props: {},
  data() {
    return {
      isFlag: false,
      choIndex: "",
      heads: [
        { t1: this.$t("had.li1"), name: "index", rot: ["/"] },
        { t1: this.$t("had.li2"), name: "product", rot: ["/product"] },
        { t1: this.$t("had.li3"), name: "docs", rot: ["/docs"] },
        { t1: this.$t("had.li4"), name: "ecoPartner", rot: ["/ecoPartner"] },
        {
          t1: this.$t("had.li5"),
          name: "",
          rot: ["/dac", "/member", "/sonior"],
        },
        { t1: this.$t("had.li6"), name: "tokens", rot: ["/tokens"] },
        {
          t1: this.$t("had.li7"),
          name: "",
          rot: ["/news", "/newsletter", "/team"],
        },
      ],
    };
  },
  computed: {},
  methods: {
    hrefCli(item) {
      window.location.href = item;
    },
    goJi(num) {
      num == this.choIndex ? (this.choIndex = "") : (this.choIndex = num);
    },
    goTo(num) {
      console.log(num);
      if ([4, 6].includes(num)) {
        num == this.choIndex ? (this.choIndex = "") : (this.choIndex = num);
      }
    },
  },
  watch: {
    $route() {
      this.isFlag = false;
    },
  },
  created() {},
  mounted() {},
};
</script>
<style scoped>
.pc {
  display: block;
}
.mob_Head {
  display: none;
}
@media screen and (max-width: 600px) {
  .pc {
    display: none;
  }
  .mob_Head {
    padding: 0px 10px;
    width: 100vw;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .moblie-nav-wrap {
    width: 0vw;
    height: 0%;
    position: fixed;
    top: 0px;
    left: 0px;
    width: 0px;
    height: 0px;
    overflow: hidden;
    z-index: 10000;
  }
  .showAp {
    width: 100vw;
    height: 100%;
  }
  .modal-layer-1 {
    position: absolute;
    width: 100%;
    height: 100%;
    background: #0b0d19;
    opacity: 0;
    left: 0px;
    top: 0px;
    z-index: 1;
  }
  .showAp .modal-layer-1 {
    opacity: 0.8;
  }
  .showAp .modal-layer-2 {
    opacity: 1;
  }
  .showAp .modal-layer-3 {
    left: 0;
  }
  .modal-layer-2 {
    position: absolute;
    width: 20%;
    right: 0px;
    top: 40px;
    z-index: 100;
    text-align: center;
    opacity: 0;
  }
  .modal-layer-2 img {
    display: block;
    height: 50px;
    padding: 10px;
    margin: 0 auto;
  }
  .modal-layer-3 {
    position: absolute;
    width: 80%;
    left: 0px;
    top: 0px;
    background: #0b0d19;
    height: 100%;
    z-index: 100;
    left: -80%;
    transition: all 0.8s;
  }
  .modal-layer-3 ul {
    padding-left: 5%;
    padding-right: 5%;
  }
  .modal-layer-3 ul li {
    border-bottom: 1px solid #232530;
  }
  .modal-layer-3 ul li a {
    display: block;
    height: 40px;
    color: #ffffff;
    line-height: 40px;
    padding-left: 5%;
  }
  .moblie-select {
    background: url("/mobile/index/plus.png") no-repeat 95% center;
  }
  .selectShow {
    background: url("/mobile/index/reduce.jpg") no-repeat 95% center;
  }
  .moblie-select-list {
    max-height: 0px;
    transition: all 0.4s;
    overflow: hidden;
  }
  .selectList {
    max-height: 200px;
  }
  .moblie-select-list a {
    font-size: 12px;
  }
}
.container {
  padding-top: 80px;
}
header {
  width: 100vw;
  height: 80px;
  background-color: #ffffff;
  top: 0;
  left: 0;
  position: fixed;
  z-index: 99;
}
.fontsix {
  width: 100px;
  font-size: 14px;
  cursor: pointer;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #333333;
  position: relative;
}
.fontsix:hover {
  color: #80d7ff;
}
.logoImg {
  width: 100px;
  margin-right: 40px;
}
/* -- */
/* .fontS3:hover .about3 {
  display: block;
} */
.fontS4:hover .about4 {
  display: block;
}
.fontS6:hover .about {
  display: block;
}

.fontS2:hover .docs {
  display: block;
}
.menu-nav-first-ab {
  position: absolute;
  width: 180px;
  /* min-height: 180px; */
  background: #333333;
  top: 80px;
  left: 0px;
  border-top: 3px solid #80d7ff;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
  padding: 10px 20px;
  text-align: left;
  display: none;
}

.menu-nav-first-ab a {
  display: block;
  height: 40px;
  line-height: 40px;
  color: #ffffff;
  font-size: 12px;
}
.menu-nav-first-ab a:hover {
  color: #80d7ff;
}
.disable {
  color: grey;
}
/* -- */
</style>
