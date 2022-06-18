<!--
* about news h-
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="padd-tb-ba malrCont pcNews">
      <h1 class="margin-bottom-liu text-center">{{ $t("h.newsList.a") }}</h1>
      <div
        v-for="(item, index) in $t('h.newsList.bList')"
        :key="index"
        class="wow fadeInUp pointer"
      >
        <div v-if="item.hrefs" @click="hrefCli(item.hrefs)" class="docCont">
          <img class="fileImg" src="/ecoPartner/img-filecoi.png" />
          <div>
            <h4 class="margin-bottom-xs">{{ item.content }}</h4>
            <p class="fontSize-14 colo999">{{ item.source }}</p>
          </div>
        </div>

        <NuxtLink
          v-else
          :to="localePath({ name: item.toLink })"
          class="docCont"
        >
          <img class="fileImg" src="/ecoPartner/img-filecoi.png" />
          <div>
            <h4 class="margin-bottom-xs">{{ item.content }}</h4>
            <p class="fontSize-14 colo999">{{ item.source }}</p>
          </div>
        </NuxtLink>
      </div>
    </div>
    <div class="mobCont padding-tb mobNews">
      <h2 class="margin-bottom text-center">{{ $t("h.newsList.a") }}</h2>
      <div
        v-for="(item, index) in $t('h.newsList.bList')"
        :key="index"
        class="wow fadeInUp"
      >
        <div v-if="item.hrefs" @click="hrefCli(item.hrefs)" class="docCont">
          <img class="fileImg" src="/ecoPartner/img-filecoi.png" />
          <div>
            <h4 class="margin-bottom-xs">{{ item.content }}</h4>
            <p class="fontSize-14 colo999">{{ item.source }}</p>
          </div>
        </div>

        <NuxtLink
          v-else
          :to="localePath({ name: item.toLink })"
          class="docCont"
        >
          <img class="fileImg" src="/ecoPartner/img-filecoi.png" />
          <div>
            <h4 class="margin-bottom-xs">{{ item.content }}</h4>
            <p class="fontSize-14 colo999">{{ item.source }}</p>
          </div>
        </NuxtLink>
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
.pcNews {
  display: block;
}
.mobNews {
  display: none;
}
@media screen and (max-width: 600px) {
  .pcNews {
    display: none;
  }
  .mobNews {
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
  color: #333333;
}
.fileImg {
  height: 80px;
}
</style>
