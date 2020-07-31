<template>
  <Page>
    <ActionBar title="Carousel Component"/>
    <GridLayout columns="*" rows="*">
      <Carousel
        row="0"
        col="0"
        debug="true"
        height="100%"
        width="100%"
        showIndicator="true"
        indicatorColor="#ddd"
        iosOverflowSafeArea="false"
        ios:finite="true"
        ios:bounce="true"
    >
        <CarouselItem v-for="(item, i) in items" :key="i" verticalAlignment="top" height="100%">
          <component :is="item" :index="i" />
        </CarouselItem>
      </Carousel>
    </GridLayout>
  </Page>
</template>

<script lang="ts">
import Vue from 'nativescript-vue'
import List from './List.vue'

export default Vue.extend({
  data() {
    return {
      items: [List, List, List]
    }
  }
})
</script>

<style scoped>
  ActionBar {
      background-color: #53ba82;
      color: #ffffff;
  }
</style>
