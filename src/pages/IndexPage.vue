<template>
  <q-layout>
    <div class="home-banner">
      <TopHeader />

      <q-item class="banner-text-section custom-container">
        <div class="col-sm-7 col-12">
          <div class="tooltip" v-if="showToolTip">
            풀타임, 파트타임!
          </div>
          <h3 class="banner-title">최고의 실력을 가진 <br />외국인 인재를 찾고 계신가요?</h3>
          <h5 class="banner-subtitle">법률 및 인사관리 부담없이 <br />1주일 이내에 원격으로 채용해보세요.</h5>
          <q-btn flat color="white" class="banner-button hide-mobile" label="개발자가 필요하신가요?" />

          <q-item class="banner-grid row q-pl-none hide-mobile">
            <div class="col-3 grid-section">
              <h5 class="q-ma-none">평균 월 120만원</h5>
              <p>임금을 해당 국가를 기준으로 계산합니다.</p>
            </div>
            <div class="col-3 grid-section">
              <h5 class="q-ma-none">최대 3회 인력교체</h5>
              <p>막상 채용해보니 맞지 않아도 걱정하지 마세요.</p>
            </div>
            <div class="col-3 grid-section">
              <h5 class="q-ma-none">평균 3일, 최대 10일</h5>
              <p>급하게 사람이 필요한 경우에도 빠른 채용이 가능합니다.</p>
            </div>
          </q-item>
        </div>

        <div class="col-sm-5 col-12 banner-slider">
          <div class="tooltip-slider" v-if="showToolTip">
            <img src="../assets/icons/dollar.png" />월 100만원
          </div>
          <carousel :itemsToShow="3" :wrapAround="true">
            <slide :key="1">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="2">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="3">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="4">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
            <slide :key="5">
              <div class="carousel__item">
                <img src="../assets/banner-user-thumb.png" />
              </div>
            </slide>
          </carousel>
        </div>
      </q-item>

      <div class="banner-bottom-slider-wrapper custom-container hide-mobile">
        <carousel :items-to-show="2.5" :autoplay="5000" :wrap-around="true">
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>해외 마케팅</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>퍼블리셔</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>캐드원(제도사)</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>해외 세일즈</span>
          </slide>
          <slide :key="1" class="bottom-slider-slide">
            <img src="../assets/icons/charts-icon.png" />
            <span>해외 CS</span>
          </slide>
        </carousel>
      </div>
    </div>

    <BottomFooter />
  </q-layout>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import TopHeader from 'src/components/TopHeader.vue';
import BottomFooter from 'src/components/BottomFooter.vue';

const showToolTip = ref(false);
onMounted(() => {
  setTimeout(() => {
    showToolTip.value = true;
  }, 500);

});

defineOptions({
  name: 'IndexPage',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
});
</script>
