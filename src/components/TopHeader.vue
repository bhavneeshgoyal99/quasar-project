<template>
  <q-header class="bg-transparent custom-container header">
    <q-toolbar class="flex justify-between">
      <img src="../assets/logo-white.png" class="header-logo">

      <div class="q-pa-md hide-mobile">
        <q-btn-dropdown class="q-mr-xl" flat color="white" label="채용">
          <q-list>
            <q-item clickable v-close-popup @click="onItemClick">
              <q-item-section>
                <q-item-label>채용</q-item-label>
              </q-item-section>
            </q-item>

            <q-item clickable v-close-popup @click="onItemClick">
              <q-item-section>
                <q-item-label>해외 개발자 원격 채용</q-item-label>
              </q-item-section>
            </q-item>

            <q-item clickable v-close-popup @click="onItemClick">
              <q-item-section>
                <q-item-label>외국인 원격 채용 (비개발 직군)</q-item-label>
              </q-item-section>
            </q-item>

            <q-item clickable v-close-popup @click="onItemClick">
              <q-item-section>
                <q-item-label>한국어 가능 외국인 채용</q-item-label>
              </q-item-section>
            </q-item>
          </q-list>
        </q-btn-dropdown>
        <q-btn flat color="white" label="해외 개발자 활용 서비스" />
      </div>

      <q-btn color="white" class="hide-mobile q-mb-md" text-color="primary" label="문의하기" />
    </q-toolbar>
  </q-header>
</template>

<script setup>
defineOptions({
  name: "TopHeader",
});
</script>
