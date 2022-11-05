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
      for (let i = 0; i < 500; i++) {
        if (i <= 400) {

          let star = document.createElement('li');
          star.classList.add('starSmall');
          document.getElementById('squares').append(star);

          star.style.animationDuration = `${Math.round(Math.random() * 20) + 12.5}s`;
          star.style.animationDelay = `${Math.round(Math.random() * 20)}s`;
          star.style.left=`${Math.round(Math.random() * 100)}%`;

        } else if (i > 400 && i <= 475) {

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

  * {
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
  }

  #app {
    min-height: 800px;
    background-color: #1c1d25;
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
        background-color: white;
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

</style>
