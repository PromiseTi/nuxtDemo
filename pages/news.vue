<!--
* about news h-
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="padd-tb-ba malrCont">
      <h1 class="margin-bottom-liu text-center">{{ $t("h.newsList.a") }}</h1>
      <div
        v-for="(item, index) in $t('h.newsList.bList')"
        :key="index"
        class="wow fadeInUp docCont"
      >
        <img class="fileImg" src="/ecoPartner/img-news.png" />
        <div>
          <h4 class="margin-bottom-xs">{{ item.content }}</h4>
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
    return {};
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
  display: flex;
  align-items: center;
  box-shadow: 0px 2px 10px 1px rgba(163, 175, 178, 0.2);
  border-radius: 10px;
  padding: 16px;
  margin-bottom: 40px;
}
.fileImg {
  height: 80px;
}
</style>
