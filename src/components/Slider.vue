<template>
<div class="q-pa-md q-mt-xl">
    <!-- <q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      swipeable
      animated
      navigation
      autoplay
      infinite
      height="300px"
      width="900px"
      class="bg-grey-1 rounded-borders"
    >
      <q-carousel-slide :name="1" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-sm q-col-gutter no-wrap">
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/mountains.jpg" />
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/parallax1.jpg" />
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/parallax2.jpg" />
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="2" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/quasar.jpg" />
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="3" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/cat.jpg" />
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/linux-avatar.png" />
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="4" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/material.png" />
          <q-img class="rounded-borders col-4 full-height" :ratio="1" src="https://cdn.quasar.dev/img/donuts.png" />
        </div>
      </q-carousel-slide>
    </q-carousel> -->
    <div class="presenter">
      <div class="presenter__viewport row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/material.png" />
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/donuts.png" />
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/mountains.jpg" />
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/parallax1.jpg" />
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/parallax2.jpg" />
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/cat.jpg" />
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/linux-avatar.png" />
        <q-img class="rounded-borders col-md-4 col-xs-12 full-height tail" :ratio="1" src="https://cdn.quasar.dev/img/quasar.jpg" />
      </div>
    </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      slide: 1
    }
  }
}
</script>

<style lang="scss">
  .presenter {
    overflow: hidden;
    min-height: 300px;
    &__viewport {
      overflow: auto;
      min-height: inherit;

      & .tail {
        max-height: 300px;
        max-width: 300px;
      }
    }
  }
</style>
