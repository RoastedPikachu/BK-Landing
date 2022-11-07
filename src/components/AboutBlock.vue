<template>
  <section class="aboutBlock" id="About">
    <h2>Обо мне:</h2>
    <div>
      <div class="aboutBlock-text">
        <p>Мне 17 лет, я студент 2 курса КИПФин, мой родной город - Москва.</p>
        <p><i>Люблю frontend разработку и занимаюсь ей уже целых <strong>10 месяцев</strong></i>. В жизни я целеустремлённый, трудолюбивый, ответственный, пунктуальный и надёжный человек.</p>
        <p>Мой путь в этой профессии начался в 16 лет с банального Hello world в h1, а теперь я могу делать свои проекты на Vue и у меня уже есть <strong>коммерческий опыт</strong> на фрилансе</p>
        <p>Мой технологический стек: <strong>HTML, CSS (Scss), JS, Vue3 (Vuex, Vue Router, NuxtJS)</strong></p>
        <p>Мои хобби: чтение, всемирная история, настольные игры и стратегии.</p>
      </div>
      <img src="@/assets/Me.jpeg">
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutBlock',
  data() {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
  .aboutBlock {
    display: flex;
    flex-direction: column;
    margin-left: 10%;
    width: 80%;
    height: 800px;
    color: white;
    h2 {
      width: 100%;
      height: 150px;
      text-align: center;
      font-size: 38px;
      font-family: 'Lora', serif;
    }
    div {
      display: flex;
      width: 100%;
      height: 550px;
      .aboutBlock-text {
        display: flex;
        flex-direction: column;
        width: 50%;
        p {
          margin-top: 30px;
          color: #898b98;
          font-size: 20px;
          font-family: 'Open Sans', sans-serif;
        }
        p:nth-child(1) {
          margin-top: 0px;
          color: white;
          font-size: 24px;
        }
      }
    }
    img {
      margin-left: 10%;
      width: 35%;
      height: 85%;
      border-radius: 10px;
      background-color: grey;
      background-size: cover;
    }
  }

  @media(max-width: 450px) {
    .aboutBlock {
      margin-top: 50px;
      height: 1200px;
      h2 {
        height: 100px;
        font-size: 34px;
      }
      div {
        flex-direction: column; 
        height: 620px;
        .aboutBlock-text {
          width: 100%;
          p {
            font-size: 16px;
          }
          p:nth-child(1) {
            font-size: 20px;
          }
        }
        img {
          margin-top: 50px;
          margin-left: 0px;
          width: 100%;
        }
      }
    }
  }

  @media(min-width: 600px) and (max-width: 1100px) {
    .aboutBlock {
      width: 85%;
      h2 {
        font-size: 34px;
      }
      div {
        .aboutBlock-text {
          p {
            font-size: 16px;
          }
          p:nth-child(1) {
            font-size: 20px;
          }
        }
        img {
          margin-left: 5%;
          width: 40%;
          height: 75%;
        }
      }
    }
  }

  @media(min-width: 1800px) {
    .aboutBlock {
      height: 950px;
      h2 {
        font-size: 52px;
      }
      div {
        height: 600px;
        .aboutBlock-text {
          p {
            margin-top: 40px;
            font-size: 26px;
          }
          p:nth-child(1) {
            font-size: 40px;
          }
        }
        img {
          margin-left: 15%;
          width: 30%;
          height: 100%;
        }
      }
    }
  }

</style>
