<!--
* ----
* @author （cgt）
* @date 2020/7/30
-->
<template>
  <div class="dac">
    <div class="coloFFF malrCont dacCont">
      <div class="lefds">
        <h1 class="margin-bottom-sm">{{ obj.a }}</h1>
        <p class="lin-height-18">{{ obj.b }}</p>
      </div>
      <img src="/dac/dacRig.png" class="rigImg" />
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
      obj: {
        a: "SINSO DAC",
        b: "A contractual framework for community governance and incentives, enabling the creation of future data index companies based on NFT collections. It is a must-have tool for building community-governed distributed business entities that unlock tremendous value from data assets in a collective manner.",
      },
    };
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style scoped>
.dacCont {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.dac {
  height: calc(100vh - 240px);
  background: url("/dac/dacs.png") no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
}
.lefds {
  width: 450px;
}
.rigImg {
  height: 400px;
}
</style>
