<!--
* docs c
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="pcDocs">
      <div class="padd-tb-ba widthSma marlrAuto flex flex-wrap">
        <div
          v-for="(item, index) in $t('c.docList')"
          :key="index"
          class="docCont"
          :class="index % 2 == 0 && 'docRig'"
        >
          <div class="flex align-center justify-center docDiv">
            <img class="docImg" :src="'/docs/do' + index + '.png'" />
          </div>
          <h3 class="margin-bottom">{{ item.a }}</h3>
          <a @click="hrefCli(item.c)">
            <div class="hvr-float-shadow usiSon">
              <p>{{ item.b }}</p>
              <img class="usiImg2" src="/index/img-jiantou@2x.png" />
            </div>
          </a>
        </div>
      </div>
    </div>
    <div class="mobDocs">
      <div class="padding-tb flex flex-wrap mobCont">
        <div
          v-for="(item, index) in $t('c.docList')"
          :key="index"
          class="mobDocCont"
          :class="index % 2 == 0 && 'docRig'"
        >
          <div class="flex align-center justify-center mobDocDiv">
            <img style="width: 20vw" :src="'/docs/do' + index + '.png'" />
          </div>
          <p class="margin-bottom-xs mobPd">{{ item.a }}</p>
          <a @click="hrefCli(item.c)">
            <div class="hvr-float-shadow mobUsi">
              <p>{{ item.b }}</p>
              <img class="usiImg2" src="/index/img-jiantou@2x.png" />
            </div>
          </a>
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
    return {};
  },
  computed: {},
  methods: {
    hrefCli(item) {
      item && (window.location.href = item);
    },
  },
  created() {},
  mounted() {},
};
</script>
<style scoped>
.pcDocs {
  display: block;
}
.mobDocs {
  display: none;
}
@media screen and (max-width: 600px) {
  .pcDocs {
    display: none;
  }
  .mobDocs {
    display: block;
  }
  .mobDocCont {
    width: 48%;
    box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
    border-radius: 10px;
    padding: 14px 10px;
    margin-bottom: 20px;
  }
  .mobDocDiv {
    height: 160px;
    box-shadow: 0px 1px 5px 1px rgba(163, 175, 178, 0.2);
    margin-bottom: 20px;
    border-radius: 8px;
  }
  .mobPd {
    font-size: 14px;
    font-weight: bold;
    height: 40px;
  }
  .mobUsi {
    color: #00abeb;
    width: 38vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-weight: bold;
    font-size: 14px;
    border-bottom: 1px solid #00abeb;
    padding-bottom: 6px;
  }
  .usiImg2 {
    height: 10px;
  }
}
.docCont {
  width: 48%;
  height: 440px;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
  border-radius: 10px;
  padding: 40px;
  margin-bottom: 80px;
}
.docDiv {
  height: 220px;
  box-shadow: 0px 1px 5px 1px rgba(163, 175, 178, 0.2);
  margin-bottom: 40px;
  border-radius: 8px;
}
.docRig {
  margin-right: 4%;
}
.docImg {
  height: 140px;
}

.usiImg2 {
  height: 10px;
}
.usiSon {
  color: #00abeb;
  width: 180px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-weight: bold;
  border-bottom: 1px solid #00abeb;
  padding-bottom: 6px;
  cursor: pointer;
}
</style>
