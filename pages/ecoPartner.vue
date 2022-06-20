<!--
* ecoPartner   d
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="pcEco">
      <div class="padd-tb-ba widthSma marlrAuto flex flex-wrap">
        <div
          v-for="(item, index) in $t('d.ecoList')"
          :key="index"
          class="docCont"
          :class="index % 2 == 0 && 'docRig'"
        >
          <img class="docImg" :src="'/ecoPartner/eco' + index + '.png'" />
          <h3 class="margin-bottom coloBls">{{ item.a }}</h3>
          <div class="lin-height-2 fontSize-14">
            <p class="margin-bottom-sm">{{ item.b }}</p>
            <p class="margin-bottom-sm">{{ item.c }}</p>
          </div>
          <div class="usiSon">
            <p>{{ item.d }}</p>
            <img class="usiImg2" src="/index/img-jiantou@2x.png" />
          </div>
        </div>
      </div>
    </div>
    <div class="mobEco">
      <div class="padding-tb mobCont">
        <div
          v-for="(item, index) in $t('d.ecoList')"
          :key="index"
          class="mobDocCont"
          :class="index % 2 == 0 && 'docRig'"
        >
          <img class="docImg" :src="'/ecoPartner/eco' + index + '.png'" />
          <h3 class="margin-bottom coloBls">{{ item.a }}</h3>
          <div class="lin-height-2 fontSize-14">
            <p class="margin-bottom-sm">{{ item.b }}</p>
            <p class="margin-bottom-sm">{{ item.c }}</p>
          </div>
          <div class="usiSon">
            <p>{{ item.d }}</p>
            <img class="usiImg2" src="/index/img-jiantou@2x.png" />
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
    return {};
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style scoped>
.pcEco {
  display: block;
}
.mobEco {
  display: none;
}
@media screen and (max-width: 600px) {
  .pcEco {
    display: none;
  }
  .mobEco {
    display: block;
  }
  .mobDocCont {
    box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
    border-radius: 10px;
    padding: 20px;
    margin-bottom: 30px;
  }
}
.docCont {
  width: 48%;
  height: 500px;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
  border-radius: 10px;
  padding: 40px;
  margin-bottom: 80px;
}
.docRig {
  margin-right: 4%;
}
.docImg {
  height: 80px;
  margin-bottom: 30px;
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
}
</style>
