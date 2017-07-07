<template>
  <section id="fullpage" class="container">
    <div>
      <div class="hero hero-1 is-fullpage">
        <div class="container">
          <h1 class="title">
            Hug-Bug
          </h1>
        </div>
      </div>
      <div class="hero hero-2 is-fullpage">
        <div class="container">
          <img src="~assets/hopo-popo.svg" alt="">
        </div>
      </div>
      <div class="hero hero-3 is-fullpage">
        <div class="container">
          <img src="~assets/alus.svg" alt="">
        </div>
      </div>
      <div class="hero hero-3 is-fullpage">
        <div class="container">
          <img src="~assets/sydan.svg" alt="">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
  import Logo from '~components/Logo.vue'

  export default {
    components: {
      Logo
    },
    data: function () {
      return {}
    },
    mounted () {
      const config = {
        reset: true,
        duration: 500,
        scale: 2,
        easing: 'ease'
      }
      window.sr = window.ScrollReveal(config)
      window.sr.reveal('.hero-1')
      window.sr.reveal('.hero-2')
      window.sr.reveal('.hero-3')
      window.sr.reveal('.hero-4')

      window.fullpage.initialize('#fullpage', {
        // navigation
        'menu': false,
        'anchors': [],
        'navigation': false,
        'navigationPosition': 'right',
        'navigationColor': '#000',
        'navigationTooltips': [],
        'slidesNavigation': false,
        'slidesNavPosition': 'bottom',
        'scrollBar': true,

        // scrolling
        'css3': true,
        'scrollingSpeed': 700,
        'autoScrolling': true,
        'easingcss3': 'ease',
        'loopHorizontal': true,
        'touchSensitivity': 5,

        // Accessibility
        'keyboardScrolling': true,
        'recordHistory': true,

        // design
        'controlArrows': true,

        // Custom selectors
        'sectionSelector': '.is-fullpage',
        'slideSelector': '.slide',

        // events
        'afterLoad': null,
        'onLeave': null,
        'afterRender': null,
        'afterResize': null,
        'afterReBuild': null,
        'afterSlideLoad': null,
        'onSlideLeave': null
      })
    }

  }
</script>

<style>
  .container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .title {
    font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

</style>
