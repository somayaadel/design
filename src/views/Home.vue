<template>
<!--    sider-->
    <div>
  <div class="slider">
  <section>

    <b-carousel
            :arrow="arrow"
            :repeat="arrowBoth"
            :arrow-hover="arrowHover"
            :icon-pack="iconPack"
            :icon-prev="iconPrev"
            :icon-next="iconNext"
            :icon-size="iconSize">
      <b-carousel-item v-for="(carousel, i) in carousels" :key="i">

        <section class="hero is-large slider-image" :style="{ backgroundImage: `url(${require('@/assets/' + carousel.image)})` } ">

          <div class="hero-body has-text-centered">

            <h1 class="title heading-primary">{{carousel.title}}</h1>
          </div>
        </section>
      </b-carousel-item>
     </b-carousel>
  </section>
  </div>

<!--    section 2-->
    <section>
              <p class="sec2-header">EXCITING TOURS FOR ADVENTUROUS PEOPLE</p>
        <div class="row container">
            <div class="columns">
                <div class=" column is-half">
                    <span class="sec2-main">You'RE GOING TO FALL IN LOVE WITH NATURE</span>
                    <p class="sec2-sub" >
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti, provident vel! Perspiciatis deleniti placeat totam numquam ipsam! Exercitationem consequuntur.
                    </p>
                      <span class="sec2-main"> LIVE ADVENTURES LIKE YOU NEVER DID BEFORE</span>
                    <p class="sec2-sub">   Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti, provident vel! Perspiciatis deleniti placeat totam numquam ipsam!</p>
                    <span class="sec2-main"> LIVE ADVENTURES LIKE YOU NEVER DID BEFORE</span>
                    <p class="sec2-sub">   Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti, provident vel! Perspiciatis deleniti placeat totam numquam ipsam!</p>
                </div>
                <div class=" column is-half">
                    <img src="@/assets/slider1.jpg">
                </div>

            </div>

        </div>
    </section>
        <section class="section-features ">
            <div class="row columns sec3">
                <div class="column is-3">
                    <div class="feature-box">
<!--                        <i class="feature-box__icon icon-basic-world"></i>-->
                        <font-awesome-icon :icon="['fad', 'coffee']"/>

                        <h3 class="heading-tertiary u-margin-bottom-small">Explore the world</h3>
                        <p class="feature-box__text">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores illo dicta itaque doloremque ullam laborum.
                        </p>
                    </div>
                </div>
                <div class="column is-3">
                    <div class="feature-box">
                        <i class="feature-box__icon icon-basic-compass"></i>
                        <h3 class="heading-tertiary u-margin-bottom-small">Meet Nature</h3>
                        <p class="feature-box__text">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores illo dicta itaque doloremque ullam laborum.
                        </p>
                    </div>
                </div>

                <div class="column is-3">
                    <div class="feature-box">
                        <i class="feature-box__icon icon-basic-map"></i>
                        <h3 class="heading-tertiary u-margin-bottom-small">Find your way</h3>
                        <p class="feature-box__text">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores illo dicta itaque doloremque ullam laborum.
                        </p>
                    </div>
                </div>

                <div class="column is-3">
                    <div class="feature-box">
                        <i class="feature-box__icon icon-basic-heart"></i>
                        <h3 class="heading-tertiary u-margin-bottom-small">Live a healthier life</h3>
                        <p class="feature-box__text">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores illo dicta itaque doloremque ullam laborum.
                        </p>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        arrow: true,
        arrowBoth: true,
        arrowHover: true,
        iconPack: 'mdi',
        iconPrev: 'arrow-left',
        iconNext: 'arrow-right',
        iconSize: '',
        carousels: [
          { title: 'IS WHERE LIFE HAPPENS', image: 'slider1.jpg' },
          { title: 'IS WHERE LIFE HAPPENS', image: 'slider2.jpg' },
          { title: 'IS WHERE LIFE HAPPENS', image: 'slider3.jpg' },
          { title: 'IS WHERE LIFE HAPPENS', image: 'slider4.jpg' }
        ]
      }
    },
    methods: {
      getImgUrl(value) {
        return `https://picsum.photos/id/43${value}/1230/500`
      }
    }
  }
</script>
