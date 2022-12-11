<template>
  <section class="helloBlock">
    <div>
      <p class="helloBlock-topParagraph">Привет, я Борис Карабут. Frontend разработчик</p>
      <p class="helloBlock-bottomParagraph">А ещё я студент, душа компании и человек, увлечённый своим делом</p>
    </div>
    <div class="helloBlock-img" alt="Луна"></div>
  </section>
</template>

<script>
export default {
  name: 'HelloBlock',
  data() {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
@import '@/styles/variables.scss';
  .helloBlock {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-left: 10%;
    width: 80%;
    height: 750px;
    div {
      width: 50%;
      color: $txt-color-global;
      z-index: 10;
      .helloBlock-topParagraph {
        width: 100%;
        font-size: 54px;
        font-family: 'Lora', serif;
      }
      .helloBlock-bottomParagraph {
        width: 100%;
        margin-top: 30px;
        color: #898b98;
        font-size: 18px;
        font-family: 'Open Sans', sans-serif;
      }
    }
    .helloBlock-img {
      display: flex;
      justify-content: center;
      width: 45%;
      height: 60%;
      background-size: cover; 
      background-image: url('@/assets/Moon.png');
    }
  }

  @media(max-width: 475px) {
    .helloBlock {
      height: 600px;
      div {
        width: 100%;
        .helloBlock-topParagraph {
          font-size: 34px;
        }
        .helloBlock-bottomParagraph {
          font-size: 16px;
        }
      }
      .helloBlock-img {
        display: none;
      }
    }
  }

  @media(min-width: 550px) and (max-width: 1100px) {
    .helloBlock {
      height: 700px;
      div {
        margin-top: -100px;
        width: 90%;
        .helloBlock-topParagraph {
          font-size: 46px;
        }
      }
      .helloBlock-img {
        display: none;
      }
    }
  }

  @media(min-width: 1600px) and (max-width: 1899px) {
    .helloBlock {
      height: 800px;
      .helloBlock-img {
        width: 50%;
      }
    }
  }

  @media(min-width: 1800px) {
    .helloBlock {
      height: 1100px;
      div {
        margin-top: -15%;
        .helloBlock-topParagraph {
          font-size: 62px;
        }
        .helloBlock-bottomParagraph {
          font-size: 30px;
        }
      }
      .helloBlock-img {
        width: 47.5%;
      }
    }
  }
</style>
