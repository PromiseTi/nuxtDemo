<!--
* Footer
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <footer>
    <div class="pcFoot">
      <div class="marlrAuto flex justify-center padding-top-sm foots">
        <div style="margin-right: 70px">
          <h2 class="margin-bottom-sm">Contact Us</h2>
          <div class="flex">
            <div class="kuus">partner@sinso.io</div>
            <client-only>
              <el-button type="primary">Copy</el-button></client-only
            >
          </div>
        </div>
        <div class="margin-top-xl">
          <div class="flex margin-bottom-sm">
            <div
              v-for="(item, index) in li1"
              :key="index"
              class="pointer liCont"
              @click="handles(item)"
            >
              <img class="footImg" :src="'/index/foot' + index + '.png'" />
              <a class="colo222">{{ item }}</a>
            </div>
          </div>
          <div class="flex">
            <div
              v-for="(item, index) in li2"
              :key="index"
              class="pointer liCont"
              @click="handles(item)"
            >
              <img
                class="footImg"
                :src="'/index/foot' + (index + 2) + '.png'"
              />
              <a class="colo222">{{ item }}</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mobFoot">
      <h3 class="margin-top-sm margin-bottom-xs text-center">Contact Us</h3>
      <div class="flex justify-center margin-bottom-sm">
        <div class="mobKus">partner@sinso.io</div>
        <client-only> <el-button type="primary">Copy</el-button></client-only>
      </div>
      <div class="flex align-center justify-center">
        <img
          @click="handles(item)"
          :src="'/index/foot' + index + '.png'"
          v-for="(item, index) in li3"
          :key="item"
          class="mobfImgs"
        />
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "",
  components: {},
  props: {},
  data() {
    return {
      li1: ["https://twitter.com/sinsonetwork", "https://t.me/sinsonetwork"],
      li2: ["https://sinsonetwork.medium.com", "https://discord.gg/m8eqcHJ5ur"],
      li3: [],
    };
  },
  computed: {},
  methods: {
    handles(item) {
      window.location.href = item;
    },
  },
  created() {},
  mounted() {
    this.li3 = [...this.li1, ...this.li2];
  },
};
</script>
<style scoped>
.pcFoot {
  display: block;
}
.mobFoot {
  display: none;
}
@media screen and (max-width: 600px) {
  .pcFoot {
    display: none;
  }
  .mobFoot {
    display: block;
  }
  .mobKus {
    width: 180px;
    background-color: #ffffff;
    color: #333333;
    height: 40px;
    line-height: 40px;
    padding-left: 10px;
    margin-right: 20px;
    border-radius: 10px;
  }
  .mobfImgs {
    height: 30px;
    padding: 6px;
    margin: 0px 5px;
  }
}
footer {
  position: absolute;
  width: 100%;
  left: 0;
  bottom: 0;
  background-color: #e8ecef;
  height: 160px;
}
.foots {
  width: 1200px;
}
.kuus {
  width: 240px;
  background-color: #ffffff;
  color: #333333;
  height: 50px;
  line-height: 50px;
  padding-left: 10px;
  margin-right: 20px;
  border-radius: 10px;
}
.footImg {
  height: 20px;
  margin-right: 10px;
}
.liCont {
  display: flex;
  width: 350px;
}
</style>
