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
              <img class="footImg" :src="'/index/foo' + index + '.png'" />
              <a class="colo222">{{ item }}</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mobFoot"></div>
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
    };
  },
  computed: {},
  methods: {
    handles(item) {
      window.location.href = item;
    },
  },
  created() {},
  mounted() {},
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
