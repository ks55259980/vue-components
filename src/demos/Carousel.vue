<template>
  <layout>
    <x-nav slot="header">
      <div slot="title">Carousel</div>
    </x-nav>
    <x-body slot="body" style="background:#fff">
      <carousel :active="active" :pagination="true" @on-change="changeHandler" :options="options" class="swiper-demo">
        <carousel-item>
          <x-img src="http://assets.bittyos.com/images/swiper/01.jpg" class="swiper-img" />
        </carousel-item>
        <carousel-item>
          <x-img src="http://assets.bittyos.com/images/swiper/02.jpg" class="swiper-img" />
        </carousel-item><carousel-item>
          <x-img src="http://assets.bittyos.com/images/swiper/03.jpg" class="swiper-img" />
        </carousel-item><carousel-item>
          <x-img src="http://assets.bittyos.com/images/swiper/04.jpg" class="swiper-img" />
        </carousel-item><carousel-item>
          <x-img src="http://assets.bittyos.com/images/swiper/05.jpg" class="swiper-img" />
        </carousel-item>
      </carousel>
    </x-body>
  </layout>
</template>

<script>
export default {
  methods: {
    changeHandler (value) {
      this.active = value
    }
  },
  data () {
    return {
      active: 0,
      options: {
        speed: 500
      }
    }
  }
}
</script>

<style lang="scss">
  .swiper-demo{
    
  }
</style>
