<!--
* ecoPartnerDetail   d
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="padd-tb-ba malrCont pcEcoDet">
      <h1 class="margin-bottom-liu text-center">{{ obj.a }}</h1>
      <div
        v-for="(item, index) in obj.bList"
        :key="index"
        class="docCont"
        :class="index % 2 == 0 && 'docRig'"
      >
        <img class="fileImg" src="/ecoPartner/img-filecoi.png" />
        <div>
          <h4 class="margin-bottom-xs">{{ item.content }}</h4>
          <p class="fontSize-14 colo999">{{ item.source }}</p>
        </div>
      </div>
    </div>
    <div class="mobCont padding-tb mobEcoDet">
      <h2 class="margin-bottom text-center">{{ obj.a }}</h2>
      <div
        v-for="(item, index) in obj.bList"
        :key="index"
        class="docCont"
        :class="index % 2 == 0 && 'docRig'"
      >
        <img style="height: 70px" src="/ecoPartner/img-filecoi.png" />
        <div>
          <h4 class="margin-bottom-xs text-ellipsis-2">{{ item.content }}</h4>
          <p class="fontSize-14 colo999">{{ item.source }}</p>
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
    };
  },
  computed: {},
  methods: {
    init() {
      let index = parseInt(this.$route?.query?.index || 0);
      console.log(index);
      this.obj = this.$t("d.doDeta")[index];
    },
  },
  created() {
    this.init();
  },
  mounted() {},
};
</script>
<style scoped>
.pcEcoDet {
  display: block;
}
.mobEcoDet {
  display: none;
}
@media screen and (max-width: 600px) {
  .pcEcoDet {
    display: none;
  }
  .mobEcoDet {
    display: block;
  }
}
.docCont {
  display: flex;
  align-items: center;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
  border-radius: 10px;
  padding: 16px;
  margin-bottom: 30px;
}
.fileImg {
  height: 80px;
}
</style>
