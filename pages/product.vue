<!--
* product b
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div>
    <div class="text-center padd-tb-ba">
      <h1 class="margin-bottom-xl">{{ $t("b.proh") }}</h1>
      <div class="lin-height-2 margin-bottom-xl">
        <p>{{ $t("b.pro1") }}</p>
        <p>{{ $t("b.pro2") }}</p>
        <p>{{ $t("b.pro3") }}</p>
        <p>{{ $t("b.pro4") }}</p>
      </div>
      <img style="width: 700px" src="/product/img-product.png" />
    </div>
    <div class="widthSma marlrAuto">
      <div
        v-for="(item, index) in $t('b.prList')"
        :key="index"
        class="flex align-center justify-between margin-bottom-qi"
        :class="index % 2 == 0 && 'flex-reverse'"
      >
        <img class="prodImg" :src="'/product/p' + index + '.png'" />
        <div class="lin-height-18 prodDi">
          <h2 class="margin-bottom">{{ item.a }}</h2>
          <p>{{ item.b }}</p>
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
.prodImg {
  height: 380px;
}
.prodDi {
  width: 480px;
}
</style>
