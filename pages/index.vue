<template>
  <div>
    <div class="pcIndex">
      <div class="flex justify-between malrCont swipes">
        <div class="flex flex-direction justify-center">
          <h1 style="font-size: 50px" class="margin-bottom">
            {{ $t("a.h1") }}
          </h1>
          <h2 class="margin-bottom-sm">{{ $t("a.h2") }}</h2>
          <h2 class="margin-bottom-sm">{{ $t("a.h3") }}</h2>
          <p>
            <a class="lians">{{ $t("a.h4") }}</a>
          </p>
        </div>
        <img class="banner" src="/index/img-home-banner@2x.png" />
      </div>
      <div class="backF3f5 padd-tb-ba">
        <div class="malrCont">
          <h1 class="text-center">{{ $t("a.pow1") }}</h1>
          <h1 class="text-center margin-bottom-liu">{{ $t("a.pow2") }}</h1>
        </div>
        <div class="flex flex-wrap malrCont">
          <div
            v-for="(item, index) in $t('a.list')"
            class="hvr-rotate poCont"
            :class="index % 2 == 0 && 'rig10'"
            :key="index"
          >
            <div class="widDi">
              <img :src="'/index/pew' + index + '.png'" />
            </div>

            <h2 class="margin-tb-sm">{{ item.powt1 }}</h2>
            <div class="lin-height-18">
              <p>{{ item.powt2 }}</p>
              <p>{{ item.powt3 }}</p>
              <p>{{ item.powt4 }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="padd-tb-ba text-center malrCont">
        <h1>{{ $t("a.infoh1") }}</h1>
        <h1 class="margin-bottom-liu">{{ $t("a.infoh2") }}</h1>
        <div class="flex justify-between margin-bottom-xl example1">
          <div
            v-for="(item, index) in $t('a.info1')"
            class="flex flex-direction justify-center wow fadeInUp inCont"
            :data-wow-delay="index * 0.2 + 0.1 + 's'"
            :key="index"
          >
            <h2>
              <countTo
                ref="example1"
                separator=""
                :start-val="0"
                :end-val="item.a"
                :duration="2000"
              />
            </h2>
            <p class="margin-tb-sm">{{ item.b }}</p>
          </div>
        </div>
        <div class="flex justify-between margin-bottom-xl example2">
          <div
            v-for="(item, index) in $t('a.info2')"
            class="flex flex-direction justify-center wow fadeInUp inCont"
            :key="index"
            :data-wow-delay="index * 0.2 + 0.1 + 's'"
          >
            <h2>
              <countTo
                ref="example2"
                separator=""
                :start-val="0"
                :end-val="item.a"
                :duration="2000"
              />
            </h2>
            <p class="margin-tb-sm">{{ item.b }}</p>
          </div>
        </div>
      </div>
      <div class="backF3f5 padd-tb-ba">
        <div class="malrCont">
          <h1 class="text-center margin-bottom-qi">{{ $t("a.usi1") }}</h1>
          <div class="flex justify-between">
            <div class="usiLeft">
              <h1 class="usleftTop">SINSO GETWAY API</h1>
              <div class="lin-height-18 fontSize-14 usleftBott">
                <p>
                  new_element = document.<span class="coloBlu"
                    >createElement</span
                  >('script')
                </p>
                <p>
                  new_element.<span class="coloBlu">setAttribute</span>('type',
                  'text/javascript')
                </p>
                <p>
                  new_element.<span class="coloBlu">setAttribute</span>('src',
                  'jQuery1.11.3.min.js')
                </p>
                <p>
                  document.body.<span class="coloBlu">appendChild</span
                  >(new_element)
                </p>
                <p>
                  <span class="coloRe">const</span> $contentType = 'image/jpg'
                </p>
                <p><span class="coloRe">const</span> $token = ''</p>
                <p><span class="coloRe">const</span> $fileName = 'phone.jpg'</p>
                <p>
                  <span class="coloRe">const</span> $url =
                  'https://api-ap-seoul-1.getway.sinso.io'
                </p>
                <p>
                  <span class="coloRe">const</span> $data =
                  '@/C:/Users/HASEE/Desktop/phone.jpg'
                </p>
                <p>
                  function upload($contentType,$token, $fileName, $url, $data) {
                </p>
                <p>$.ajax({</p>
                <p>url: `${$url}/v1/upload?name=${$fileName}`,</p>
                <p>type: 'POST',</p>
                <p>dataType:'json',</p>
                <p>headers: {</p>
                <p>Token: $token, 'Content-Type': $contentType,</p>
                <p>},</p>
                <p>data: $data,</p>
                <p>success: (res) => {</p>
                <p><span class="coloRe">if</span> (res.code == 200) {</p>
                <p>console.log(res)</p>
                <p>}</p>
                <p>}</p>
                <p>})</p>
                <p>}</p>
              </div>
            </div>
            <div class="usiRight">
              <NuxtLink to="/">
                <div class="flex margin-bottom-qi">
                  <img class="usiImg1" src="/index/usi5.png" />
                  <div class="hvr-float-shadow usiSon">
                    <p>Dev docs</p>
                    <img class="usiImg2" src="/index/img-jiantou@2x.png" />
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink to="/">
                <div class="flex margin-bottom-xl">
                  <img class="usiImg1" src="/index/usi3.png" />
                  <div class="hvr-float-shadow usiSon">
                    <p>Testnet</p>
                    <img class="usiImg2" src="/index/img-jiantou@2x.png" />
                  </div>
                </div>
              </NuxtLink>
              <img class="usiImg3" src="/index/usi2.png" />
            </div>
          </div>
        </div>
      </div>
      <div class="padd-tb-ba ecolCont">
        <div class="malrCont">
          <h1 class="coloFFF text-center margin-bottom-qi">
            {{ $t("a.byh") }}
          </h1>
          <client-only>
            <swiper class="swiper" :options="swiperOption1">
              <swiper-slide
                id="elItem"
                class="swiper-slide"
                v-for="(item, index) in $t('a.byList')"
                :key="index"
              >
                <img :src="'/index/ol' + index + '.png'" />
                <div class="lin-height-18">
                  <p>{{ item.a1 }}</p>
                  <p>{{ item.a2 }}</p>
                  <p>{{ item.a3 }}</p>
                  <p>{{ item.a4 }}</p>
                </div>

                <el-button round class="margin-top">Learn more</el-button>
              </swiper-slide>

              <div
                class="swiper-pagination swiper-pagination-white"
                slot="pagination"
              ></div>
              <div class="swiper-button-prev" slot="button-prev"></div>
              <div class="swiper-button-next" slot="button-next"></div>
            </swiper>
          </client-only>
        </div>
      </div>
      <div class="backF3f5 padd-tb-ba">
        <div class="malrCont">
          <h1 class="text-center margin-bottom-qi">{{ $t("a.roah") }}</h1>
          <div class="roaCont">
            <client-only>
              <swiper class="swiper" :options="swiperOption2">
                <swiper-slide
                  v-for="(item, index) in $t('a.roaList')"
                  :key="index"
                  id="roaItem"
                >
                  <div class="roaPos">
                    <div>
                      <img src="/index/dianTrue.png" />
                      <p
                        :class="index == tabsIndex && 'coloBls'"
                        class="fontBlod fontSize-20"
                      >
                        {{ item.a }}
                      </p>
                    </div>
                  </div>
                  <div
                    class="lin-height-2 raoJiu"
                    :class="index == tabsIndex && 'roBjo'"
                    @click="tabsIndex = index"
                  >
                    <div class="margin-bottom">
                      <p v-for="itemm in item.b" :key="itemm">{{ itemm }}</p>
                    </div>
                    <p v-for="itemm in item.c" :key="itemm">{{ itemm }}</p>
                  </div>
                </swiper-slide>
              </swiper>
              <div class="swiper-button-prev swipe-prev2"></div>
              <div class="swiper-button-next swipe-next2"></div>
            </client-only>
          </div>
          <p
            class="marlrAuto margin-tb-xl hvr-wobble-horizontal widbutt"
            style="display: flex"
            @click="hrefCli('https://github.com/sinsoio')"
          >
            <img src="/index/githubs.png" /> {{ $t("a.toagit") }}
          </p>
        </div>
      </div>
      <div class="backF3f5 padd-tb-ba">
        <div class="malrCont">
          <h1 class="text-center margin-bottom-qi">{{ $t("a.edyh") }}</h1>
          <div class="flex flex-wrap">
            <img
              class="hvr-grow-shadow byImg"
              :class="(index + 1) % 5 != 0 && 'bymar'"
              v-for="(item, index) in 17"
              :key="index"
              :src="'/index/by' + index + '.png'"
            />
          </div>
        </div>
      </div>
      <div class="backF3f5 padd-tb-ba newCont">
        <div class="malrCont">
          <h1 class="text-center margin-bottom-qi">{{ $t("a.newh") }}</h1>
          <div class="flex justify-between">
            <div
              v-for="(item, index) in $t('a.newList')"
              :key="index"
              class="hvr-float-shadow newItem"
              @click="hrefCli(item.c)"
            >
              <img class="neback" :src="'/index/bot' + index + '.jpg'" />

              <div class="lin-height-18 fontDize-14">
                <p class="colo999">{{ item.a }}</p>
                <p class="margin-bottom-xs">{{ item.b }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mobIndex">
      <div class="text-center mobTop">
        <img style="width: 100%" src="/index/img-home-banner@2x.png" />
        <h1 class="margin-tb-sm">{{ $t("a.h1") }}</h1>
        <h3>{{ $t("a.h2") }}</h3>
        <h3 class="margin-top-xs margin-bottom-sm">{{ $t("a.h3") }}</h3>
        <p>
          <a class="lians">{{ $t("a.h4") }}</a>
        </p>
      </div>
      <div class="backF3f5 padding-tb-sm">
        <div class="text-center lin-height-16 margin-bottom-sm">
          <h3>{{ $t("a.pow1") }}</h3>
          <h3>{{ $t("a.pow2") }}</h3>
        </div>
        <div class="flex flex-wrap mobCont">
          <div
            v-for="(item, index) in $t('a.list')"
            class="mobPo"
            :class="index % 2 == 0 && 'moRig10'"
            :key="index"
          >
            <img class="mobPoImgs" :src="'/index/pew' + index + '.png'" />

            <h2 class="margin-bottom-xs">{{ item.powt1 }}</h2>
            <div class="lin-height-18 fontSize-14">
              <p>{{ item.powt2 }}</p>
              <p>{{ item.powt3 }}</p>
              <p>{{ item.powt4 }}</p>
            </div>
          </div>
        </div>
      </div>
      <div class="backFFF padding-tb-sm">
        <div class="text-center lin-height-18 margin-bottom-sm">
          <h3>{{ $t("a.infoh1") }}</h3>
          <h3>{{ $t("a.infoh2") }}</h3>
        </div>
        <div
          v-for="(item, index) in $t('a.info1')"
          class="marlrAuto mobIn"
          :key="index"
        >
          <h2>
            <countTo
              ref="example1"
              separator=""
              :start-val="0"
              :end-val="item.a"
              :duration="2000"
            />
          </h2>
          <p class="margin-top-xs">{{ item.b }}</p>
        </div>
        <div
          v-for="item in $t('a.info2')"
          class="marlrAuto mobIn"
          :key="item.a"
        >
          <h2>
            <countTo
              ref="example1"
              separator=""
              :start-val="0"
              :end-val="item.a"
              :duration="2000"
            />
          </h2>
          <p class="margin-top-xs">{{ item.b }}</p>
        </div>
      </div>

      <div class="backF3f5 padding-tb-sm">
        <div class="mobCont">
          <h3 class="text-center margin-bottom-xs lin-height-18">
            {{ $t("a.usi1") }}
          </h3>
          <div class="mobUsiLeft">
            <h3 class="usleftTop">SINSO GETWAY API</h3>
            <div class="lin-height-18 fontSize-12 usleftBott">
              <p>
                new_element = document.<span class="coloBlu">createElement</span
                >('script')
              </p>
              <p>
                new_element.<span class="coloBlu">setAttribute</span>('type',
                'text/javascript')
              </p>
              <p>
                new_element.<span class="coloBlu">setAttribute</span>('src',
                'jQuery1.11.3.min.js')
              </p>
              <p>
                document.body.<span class="coloBlu">appendChild</span
                >(new_element)
              </p>
              <p>
                <span class="coloRe">const</span> $contentType = 'image/jpg'
              </p>
              <p><span class="coloRe">const</span> $token = ''</p>
              <p><span class="coloRe">const</span> $fileName = 'phone.jpg'</p>
              <p>
                <span class="coloRe">const</span> $url =
                'https://api-ap-seoul-1.getway.sinso.io'
              </p>
              <p>
                <span class="coloRe">const</span> $data =
                '@/C:/Users/HASEE/Desktop/phone.jpg'
              </p>
              <p>
                function upload($contentType,$token, $fileName, $url, $data) {
              </p>
              <p>$.ajax({</p>
              <p>url: `${$url}/v1/upload?name=${$fileName}`,</p>
              <p>type: 'POST',</p>
              <p>dataType:'json',</p>
              <p>headers: {</p>
              <p>Token: $token, 'Content-Type': $contentType,</p>
              <p>},</p>
              <p>data: $data,</p>
              <p>success: (res) => {</p>
              <p><span class="coloRe">if</span> (res.code == 200) {</p>
              <p>console.log(res)</p>
              <p>}</p>
              <p>}</p>
              <p>})</p>
              <p>}</p>
            </div>
          </div>
          <div class="flex align-center justify-between usiRight">
            <div>
              <NuxtLink to="/">
                <div class="flex margin-bottom-sm">
                  <img class="mobUsiImg1" src="/index/usi5.png" />
                  <div class="mobUsiSon">
                    <p>Dev docs</p>
                    <img class="mobUsiImg2" src="/index/img-jiantou@2x.png" />
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink to="/">
                <div class="flex">
                  <img class="mobUsiImg1" src="/index/usi3.png" />
                  <div class="mobUsiSon">
                    <p>Testnet</p>
                    <img class="mobUsiImg2" src="/index/img-jiantou@2x.png" />
                  </div>
                </div>
              </NuxtLink>
            </div>
            <img class="mobUsiImg3" src="/index/usi2.png" />
          </div>
        </div>
      </div>
      <!-- -- -->
      <div class="padding-tb mobEcolCont">
        <div class="">
          <h1 class="coloFFF text-center margin-bottom">
            {{ $t("a.byh") }}
          </h1>
          <client-only>
            <div class="mobCont">
              <swiper class="swiper" :options="mobswiperOption1">
                <swiper-slide
                  id="elItem"
                  class="swiper-slide"
                  v-for="(item, index) in $t('a.byList')"
                  :key="index"
                >
                  <img :src="'/index/ol' + index + '.png'" />
                  <div class="lin-height-18">
                    <p>{{ item.a1 }}</p>
                    <p>{{ item.a2 }}</p>
                    <p>{{ item.a3 }}</p>
                    <p>{{ item.a4 }}</p>
                  </div>
                  <el-button round class="margin-top">Learn more</el-button>
                </swiper-slide>
                <div
                  class="swiper-pagination swiper-pagination-white"
                  slot="pagination"
                ></div>
                <div
                  class="swiper-button-prev mobPer1"
                  slot="button-prev"
                ></div>
                <div
                  class="swiper-button-next mobNext1"
                  slot="button-next"
                ></div>
              </swiper>
            </div>
          </client-only>
        </div>
      </div>
      <div class="backF3f5 padding-tb">
        <div class="">
          <h3 class="text-center margin-bottom">{{ $t("a.roah") }}</h3>
          <div class="roaCont">
            <client-only>
              <swiper class="swiper" :options="mobswiperOption2">
                <swiper-slide
                  v-for="(item, index) in $t('a.roaList')"
                  :key="index"
                >
                  <div class="roaPos">
                    <div>
                      <img src="/index/dianTrue.png" />
                      <p
                        :class="index == tabsIndex && 'coloBls'"
                        class="fontBlod fontSize-20"
                      >
                        {{ item.a }}
                      </p>
                    </div>
                  </div>
                  <div
                    class="lin-height-2 raoJiu"
                    style="width: 100%; height: auto"
                    :class="index == tabsIndex && 'roBjo'"
                    @click="tabsIndex = index"
                  >
                    <div class="margin-bottom">
                      <p v-for="itemm in item.b" :key="itemm">{{ itemm }}</p>
                    </div>
                    <p v-for="itemm in item.c" :key="itemm">{{ itemm }}</p>
                  </div>
                </swiper-slide>
              </swiper>
              <div class="swiper-button-prev swipe-prev2"></div>
              <div class="swiper-button-next swipe-next2"></div>
            </client-only>
          </div>
          <p
            class="marlrAuto margin-top-xl widbutt"
            @click="hrefCli('https://github.com/sinsoio')"
          >
            <img src="/index/githubs.png" /> {{ $t("a.toagit") }}
          </p>
        </div>
      </div>
      <div class="backF3f5 padding-tb">
        <div class="mobCont">
          <h3 class="text-center margin-bottom">{{ $t("a.edyh") }}</h3>
          <div class="flex flex-wrap">
            <img
              style="width: 32%"
              class="margin-bottom-xs"
              :class="(index + 1) % 3 != 0 && 'bymar'"
              v-for="(item, index) in 17"
              :key="index"
              :src="'/index/by' + index + '.png'"
            />
          </div>
        </div>
      </div>
      <div class="backF3f5 padding-tb newCont">
        <div class="mobCont">
          <h1 class="text-center margin-bottom">{{ $t("a.newh") }}</h1>
          <div class="flex flex-wrap">
            <div
              v-for="(item, index) in $t('a.newList')"
              :key="index"
              class="margin-bottom-xs mobnewItem"
              :class="index % 2 == 0 && 'mobNewRights'"
              @click="hrefCli(item.c)"
            >
              <img class="neback" :src="'/index/bot' + index + '.jpg'" />

              <div class="lin-height-18 fontDize-14">
                <p class="colo999">{{ item.a }}</p>
                <p class="margin-bottom-xs">{{ item.b }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      tabsIndex: 1, //
      //pc 1
      swiperOption1: {
        slidesPerView: 4,
        spaceBetween: 30,
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      },
      //pc 2
      swiperOption2: {
        slidesPerView: 4,
        spaceBetween: 30,
        navigation: {
          nextEl: ".swipe-next2",
          prevEl: ".swipe-prev2",
        },
      },
      //mob 1
      mobswiperOption1: {
        slidesPerView: 1,
        spaceBetween: 30,
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      },
      //mob 2
      mobswiperOption2: {
        slidesPerView: 1,
        spaceBetween: 30,
        navigation: {
          nextEl: ".swipe-next2",
          prevEl: ".swipe-prev2",
        },
      },
    };
  },
  mounted() {
    var that = this;
    new WOW({
      live: false,
      callback(dom) {
        if (dom.className.indexOf("example1")) {
          that.$refs.example1[0].start();
          that.$refs.example1[1].start();
          that.$refs.example1[2].start();
        }
        if (dom.className.indexOf("example2")) {
          that.$refs.example2[0].start();
          that.$refs.example2[1].start();
          that.$refs.example2[2].start();
        }
      },
    }).init();
    // console.log(this);
    // console.log(this.$i18n);
  },
  methods: {
    hrefCli(item) {
      item && (window.location.href = item);
    },
  },
};
</script>
<style scoped>
h2 > span {
  font-size: 28px;
}
.pcIndex {
  display: block;
}
.mobIndex {
  display: none;
}
@media screen and (max-width: 600px) {
  .pcIndex {
    display: none;
  }
  .mobIndex {
    display: block;
  }
  .mobTop {
    width: 90vw;
    margin-left: auto;
    margin-right: auto;
    margin-top: 20px;
    margin-bottom: 30px;
  }
  .mobPo {
    width: 47%;
    background-color: #e8edf1;
    border-radius: 10px;
    padding: 10px 4px;
    margin-bottom: 20px;
  }
  .moRig10 {
    margin-right: 4%;
  }
  .mobPoImgs {
    height: 40px;
    margin: 10px 0px;
  }
  .mobIn {
    color: #ffffff;
    text-align: center;
    background: linear-gradient(135deg, #077fe3, #24beed);
    width: 80%;
    padding: 20px 0px;
    border-radius: 10px;
    margin-bottom: 16px;
  }
  .mobUsiLeft {
    border: 0.5px solid #e5e5e5;
    border-radius: 14px;
    overflow: hidden;
  }
  .mobUsiImg1 {
    width: 20px;
  }
  .mobUsiImg2 {
    height: 8px;
  }
  .mobUsiImg3 {
    width: 40vw;
  }
  .mobUsiSon {
    font-size: 14px;
    color: #00abeb;
    width: 120px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-left: 10px;
    border-bottom: 1px solid #00abeb;
  }
  .mobEcolCont {
    background: url(/index/img-homes.png) no-repeat 50%;
  }
  .mobPer1 {
    top: auto;
    left: 20px;
    bottom: 0px;
    width: auto;
  }
  .mobNext1 {
    top: auto;
    right: 20px;
    bottom: 0px;
    width: auto;
  }
  .mobnewItem {
    background-color: #fff;
    padding: 8px;
    width: 48%;
    border-radius: 8px;
  }
  .mobNewRights {
    margin-right: 2%;
  }
}
.swipes {
  height: 740px;
  font-size: 20px;
}
.banner {
  height: 600px;
}
.lians {
  cursor: pointer;
  font-size: 16px;
  border-bottom: 1px solid #333333;
}
.poCont {
  width: 47%;
  background-color: #e8edf1;
  height: 300px;
  margin-bottom: 70px;
  padding: 50px 0px 0px 60px;
  border-radius: 20px;
}
.rig10 {
  margin-right: 6%;
}
.widDi {
  height: 60px;
}
.widDi img {
  width: 40px;
}
.inCont {
  color: #ffffff;
  text-align: center;
  background: linear-gradient(135deg, #077fe3, #24beed);
  width: 32%;
  height: 160px;
  border-radius: 10px;
}
.ecolCont {
  height: 800px;
  background: url("/index/img-homes.png") no-repeat center;
}

#roaItem {
  width: 25% !important;
  margin-right: 0px !important;
}
.roaPos {
  margin-top: 30px;
  margin-bottom: 110px;
  border-top: 2px solid #00abeb;
  position: relative;
}
.roaPos > div {
  position: absolute;
  left: 0px;
  top: -20px;
  width: 100%;
  text-align: center;
}
.roaPos img {
  width: 40px;
  margin-bottom: 20px;
}
.raoJiu {
  margin-left: auto;
  margin-right: auto;
  width: 90%;
  height: 280px;
  border: 1px dashed #a1d5e8;
  border-radius: 10px;
  padding: 14px;
  font-size: 14px;
  cursor: pointer;
}
.roBjo {
  border: none;
  color: #ffffff;
  background: linear-gradient(0deg, #1dafe6 0%, #83d8f8 100%);
}
.byImg {
  width: 18%;
  margin-bottom: 30px;
}
.bymar {
  margin-right: 1%;
}
.newCont {
  background: url("/index/img-home-bg2@2x.png") no-repeat;
  background-size: cover;
}
.newItem {
  border-radius: 8px;
  background-color: #ffffff;
  padding: 20px;
  width: 24%;
  cursor: pointer;
}
.neback {
  width: 100%;
  border-radius: 10px;
  overflow: hidden;
  /* height: 140px; */
  margin-bottom: 10px;
}
.usiLeft {
  border: 0.5px solid #e5e5e5;
  border-radius: 14px;
  width: 800px;
  overflow: hidden;
}
.usleftTop {
  background-color: #252c2f;
  color: #ffffff;
  padding: 20px 0px 20px 20px;
}
.usleftBott {
  padding: 20px;
  height: 400px;
  overflow-y: scroll;
  background-color: #ffffff;
}
.usiRight {
  padding-top: 60px;
  /* width: 400px; */
}
.usiImg1 {
  width: 30px;
}
.usiImg2 {
  height: 10px;
}
.usiImg3 {
  height: 230px;
}
.usiSon {
  color: #00abeb;
  width: 180px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-left: 10px;
  border-bottom: 1px solid #00abeb;
}
/* 轮播 */
::v-deep .swiper-container {
  height: 500px;
}
.roaCont {
  border-radius: 10px;
  padding: 20px 70px 70px 70px;
  background-color: #ffffff;
  position: relative;
}
::v-deep .roaCont .swiper-container {
  height: 440px;
}
#elItem {
  height: 400px !important;
  padding: 30px;
  text-align: center;
  background: #ffffff;
  border-radius: 10px;
  overflow: hidden;
}
#elItem > img {
  height: 70px;
  margin-bottom: 30px;
}
::v-deep .ecolCont .swiper-button-prev {
  left: 30%;
  top: calc(100% - 20px);
  width: auto;
}
::v-deep .ecolCont .swiper-button-next {
  right: 30%;
  top: calc(100% - 20px);
  width: auto;
}
::v-deep .swiper-button-prev::after {
  content: "";
  background: url("/index/img-left.png") no-repeat;
  background-size: cover;
  width: 50px;
  height: 50px;
}
::v-deep .swiper-button-next::after {
  content: "";
  background: url("/index/img-right.png") no-repeat;
  background-size: cover;
  width: 50px;
  height: 50px;
}

::v-deep .roaCont .swiper-button-prev {
  left: 10px;
  top: 50px;
  width: auto;
}
::v-deep .roaCont .swiper-button-next {
  right: 10px;
  top: 50px;
  width: auto;
}
</style>
