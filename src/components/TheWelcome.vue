

<template>
  <div class="content-wrapper">
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Fairfield, Ohio</template>
      Seven Day Weather Forecast
      <RouterLink :to="{ name: 'forecast' }" @click="setCity('fairfield')"
        >Forecast</RouterLink
      >
      for Fairfield, Ohio
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Athens, Ohio</template>
      Seven Day Weather Forecast
      <RouterLink :to="{ name: 'forecast' }" @click="setCity('athens')"
        >Forecast</RouterLink
      >
      for Athens, Ohio
    </WelcomeItem>

    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Portland, Oregon</template>
      Seven Day Weather Forecast
      <RouterLink :to="{ name: 'forecast' }" @click="setCity('portland')"
        >Forecast</RouterLink
      >
      for Portland, Oregon
    </WelcomeItem>
    <WelcomeItem>
      <template #icon>
        <DocumentationIcon />
      </template>
      <template #heading>Tuscon, Arizona</template>
      Seven Day Weather Forecast
      <RouterLink :to="{ name: 'forecast' }" @click="setCity('tuscon')"
        >Forecast</RouterLink
      >
      for Tuscon, Arizona
    </WelcomeItem>
  </div>
</template>

<script setup>
import { useStore } from "vuex";
import WelcomeItem from "./WelcomeItem.vue";
import DocumentationIcon from "./icons/IconDocumentation.vue";

const store = useStore();
const setCity = (cityName) => {
  //console.log(cityName);
  store.commit("setCurrentCity", cityName);
};
</script>

<style scoped>
.content-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>