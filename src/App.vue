<template>
<div class="home">
  <HeaderMain />
  <Carousel class="carousel"  v-slot="{ currentSlide }" >
    <Slide v-for="(slide, index) in carouselSlides" :key="index">
      <div v-show="currentSlide === index + 1" class="slide-info">
          <img :src="require(`./assets/${slide.name}.png`)" :alt="slide.webSiteName">
          <a class="site-url" :href="slide.siteUrl" target="_blank">VIEW LIVE</a>
      </div>
    </Slide>
  </Carousel>
  <div class="gallery-wrapper">
    <Gallery class="gallery">
      <Image class="image" v-for="(image, ind) in galleryImages" :key="ind">
        <img :src="require(`./assets/${image.name}.png`)" :alt="image.name">
      </Image>
    </Gallery>
  </div>
</div>
</template>

<script>
import HeaderMain from "./components/Header"
import Carousel from "./components/Carousel"
import Slide from "./components/Slide"
import Gallery from "./components/Gallery.vue"
import Image from "./components/Image.vue"
import Masonry from "masonry-layout"

<<<<<<< HEAD
window.onload = () => {
    const grid = document.querySelector('.gallery');

    const masonry = new Masonry(grid, {
      itemSelector: ".image",
      fitWidth: true,
      gutter: 0

    });

    return { masonry }
}

=======
>>>>>>> 459e49324ad5fb9d7ec30be52a1ffb434d8e6724
export default {
  name: 'App',
  components: {
    HeaderMain,
    Carousel,
    Slide,
    Gallery,
    Image,
    
  },
  setup() {
    // const carouselSlides = ["ws-1", "ws-2", "ws-3", "ws-4", "ws-5", "ws-6", "ws-7", "ws-8"];
    const carouselSlides = [
      {
        name: "ws-1",
        webSiteName: "mysmartswimwear",
        siteUrl: "//mysmartswimwear.com/"
      },
      {
        name: "ws-2",
        webSiteName: "cryptalo",
        siteUrl: "//cryptalo.com/"
      },
      {
        name: "ws-3",
        webSiteName: "digikeymarket",
        siteUrl: "//digikeymarket.com/"
      },
      {
        name: "ws-4",
        webSiteName: "investmedia",
        siteUrl: "//investmedia.tech/"
      },
      {
        name: "ws-5",
        webSiteName: "fxbrokerrating",
        siteUrl: "//fxbrokerrating.com/"
      },
      {
        name: "ws-6",
        webSiteName: "trendingbrokers",
        siteUrl: "//trendingbrokers.com/"
      },
      {
        name: "ws-7",
        webSiteName: "guiadeltrading",
        siteUrl: "//guiadeltrading.com/"
      },
      {
        name: "ws-8",
        webSiteName: "forexinspect",
        siteUrl: "//forexinspect.com/"
      },
    ];

    const galleryImages = [
      {
        name: "img-01"
      },
      {
        name: "img-02"
      },
      {
        name: "img-03"
      },
      {
        name: "img-04"
      },
      {
        name: "img-05"
      },
      {
        name: "img-06"
      },
      {
        name: "img-07"
      },
      {
        name: "img-08"
      },
      {
        name: "img-09"
      },
      {
        name: "img-10"
      },
      {
        name: "img-11"
      },
      {
        name: "img-12"
      },
      {
        name: "img-13"
      },
      {
        name: "img-14"
      },
      {
        name: "img-15"
      },
      {
        name: "img-16"
      },
      {
        name: "img-17"
      },
      {
        name: "img-18"
      },
      {
        name: "img-19"
      },
      {
        name: "img-20"
      },
      {
        name: "img-21"
      }
    ];

    return { carouselSlides, galleryImages }
  }
}
</script>

<style lang="scss">


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-top: 40px;
}

.container {
  max-width: 1366px;
  margin: auto;
  padding: 0 40px;
}

.d-f {
  display: flex;
}

.d-fc {
  display: flex;
  align-items: center;
  justify-content: center;
}

.d-fsb {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.carousel {
  position: relative;
  height: auto;

  .slide {
    display: flex;
    align-items: center;
    justify-content: center;

    .slide-info {
      width: 100%;
      max-width: 1000px;
      height: auto;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

      .site-url {
        // color: #FFD600;
        position: relative;
        color: #333;
        text-decoration: none;
        padding: 10px 15px;
        font-weight: 500;
        border: 1px solid #333;
        z-index: 0;

        &::before {
          content: "";
          position: absolute;
          left: 0;
          top: 0;
          width: 100%;
          height: 100%;
          background: #fff;
          z-index: -1;
          transition: .4s all;
        }

        &:hover::before {
          background-color: #333;
        }

        &:hover {
          transition: .4s all;
          color: #FFD600;
        }
      }
    }
  }
}
.gallery-wrapper {
  background: #333;
  padding: 40px;
  margin-top: 70px;

  .gallery {
      margin: 40px auto;

      .image {
        width: 30%;

        img {
          width: 100%;
        }
      }
  }
}

</style>
