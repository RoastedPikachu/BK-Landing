<template>
  <HeaderComp/>

  <ContactIcons/>

  <ul id="squares"></ul>

  <HelloBlock/>

  <AboutBlock/>

  <MyProjectsBlock/>

  <FooterComp/>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue';
import ContactIcons from './components/ContactIcons.vue';
import HelloBlock from './components/HelloBlock.vue';
import AboutBlock from './components/AboutBlock.vue';
import MyProjectsBlock from './components/MyProjectsBlock.vue';
import FooterComp from './components/FooterComp.vue';

export default {
  name: 'App',
  data() {  
    return {
      
    }
  },
  methods: {
    createStars() {
      for (let i = 0; i < 400; i++) {
        if (i <= 325) {

          let star = document.createElement('li');
          star.classList.add('starSmall');
          document.getElementById('squares').append(star);

          star.style.animationDuration = `${Math.round(Math.random() * 20) + 12.5}s`;
          star.style.animationDelay = `${Math.round(Math.random() * 20)}s`;
          star.style.left=`${Math.round(Math.random() * 100)}%`;

        } else if (i > 325 && i <= 375) {

          let star = document.createElement('li');
          star.classList.add('starMedium');
          document.getElementById('squares').append(star);

          star.style.animationDuration = `${Math.round(Math.random() * 20) + 12.5}s`;
          star.style.animationDelay = `${Math.round(Math.random() * 20)}s`;
          star.style.left=`${Math.round(Math.random() * 100)}%`;

        } else {

          let star = document.createElement('li');
          star.classList.add('starLarge');
          document.getElementById('squares').append(star);

          star.style.animationDuration = `${Math.round(Math.random() * 20) + 12.5}s`;
          star.style.animationDelay = `${Math.round(Math.random() * 6)}s`;
          star.style.left=`${Math.round(Math.random() * 100)}%`;
        }
      }
      
    }
  },
  mounted() {
    this.createStars();
  },
  components: {
    HeaderComp,
    ContactIcons,
    HelloBlock,
    AboutBlock,
    MyProjectsBlock,
    FooterComp,
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lora:wght@400;600&family=Open+Sans:wght@400;600&display=swap');
@import './styles/variables.scss';

  * {
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
  }

  #app {
    min-height: 800px;
    background-color: $bg-color-global;
    #squares {
      position: absolute;
      width: 100%;
      height: 85%;
      list-style: none;
      overflow: hidden;
      li {
        position: absolute;
        bottom: -150px;
        border-radius: 100%;
        background-color: $txt-color-global;
        animation: animate 25s linear infinite;
      }
      .starBig {
        width: 7.5px;
        height: 7.5px;
        animation-delay: 2s;
        animation-duration: 20s;
      }
      .starMedium {
        width: 5px;
        height: 5px;
        animation-delay: 1s;
        animation-duration: 15s;
      }
      .starSmall {
        width: 2.5px;
        height: 2.5px;
        animation-delay: 0;
        animation-duration: 10s;
      }
      @keyframes animate {
        0% {
          transform: translateY(0) rotate(0deg);
          opacity: 0.9;
        }
        100% {
          transform: translateY(-1000px) rotate(720deg);
          opacity: 0;
        }
      }
    }
  }

  @media(max-width: 475px) {
    #app {
      #squares {
        height: 80%;
      }
    }
  }

  @media(min-width: 600px) and (max-width: 1100px) {
    #app {
      #squares {
        height: 90%;
      }
    }
  }

  @media(min-height: 800px) and (max-height: 1000px) {
    #app {
      #squares {
        height: 90%;
      }
    }
  }

  @media(min-height: 1200px) and (max-height: 1399px) {
    #app {
      #squares {
        height: 75%;
      }
    }
  }

  @media(min-height: 1400px) and (max-height: 1599px) {
    #app {
      #squares {
        height: 67.5%;
      }
    }
  }

  @media(min-height: 1600px) and (max-height: 1799px) {
    #app {
      #squares {
        height: 60%;
      }
    }
  }

  @media(min-height: 1800px) and (max-height: 2100px) {
    #app {
      #squares {
        height: 50%;
      }
    }
  }

</style>
