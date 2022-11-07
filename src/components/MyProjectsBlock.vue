<template>
  <section class="myProjectsBlock" id="Projects">
    <h2>Последние проекты:</h2>
    <a href="https://github.com/RoastedPikachu/To-Do-List-v2.0">
      <div id="myProjectsBlock-firstImage" title="To do list" alt="To do list"> 
        <div></div>
        <p><strong>To-Do-List-v2.0</strong></p>
        <p>Список дел</p>
        <p>01</p>
      </div>
    </a>
    <a href="https://github.com/RoastedPikachu/WeatherMeteo">
      <div id="myProjectsBlock-secondImage" title="Weather Meteo" alt="Weather Meteo">
        <div></div>
        <p><strong>WeatherMeteo</strong></p>
        <p>Сайт прогноза погоды</p>
        <p>02</p>
      </div>
    </a>
  </section>
</template>

<script>
export default {
  name: 'MyProjectsBlock',
  data() {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
  .myProjectsBlock {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 1570px;
    background-color: rgb(255, 241, 226);
    h2 {
      margin-top: 100px;
      width: 100%;
      height: 150px;
      color: #1c1d25;
      font-size: 38px;
      font-family: 'Lora', serif;
      text-align: center;
    }
    a {
      position: relative;
      margin-left: 10%;
      width: 65%;
      height: 550px;
      div {
        display: flex;
        justify-content: flex-start;
        width: 100%;
        height: 100%;
        border-radius: 10px;
        border: 0;
        background-image: linear-gradient(rgba(0, 0, 0, .6), rgba(0, 0, 0, .6)), url('@/assets/ToDo-list.png');
        background-size: cover;
        transition: 0.2s ease;
        overflow: hidden;
        div {
          background: linear-gradient(to right, rgba(9, 15, 33, 0.8), rgba(9, 23, 44, 0.8));
          transform: translateX(-100%);
          transition: 0.3s ease;
          z-index: 9;
        }
        p {
          position: absolute;
          margin-top: calc(40% - 10px);
          margin-left: 7.5%;
          color: white;
          font-size: 40px;
          font-family: 'Open Sans', sans-serif;
          font-weight: bold;
          text-decoration: none;
          transition: transform 0.4s, opacity 0.6s ease;
          z-index: 9;
        }
        p:nth-child(3) {
          margin-top: calc(40% + 50px);
          font-size: 32px; 
        }
        p:nth-child(4) {
          right: -15px;
          margin-top: -50px;
          color: white;
          opacity: 0;
          font-size: 202px;
        }
      }
      div:hover {     
        box-shadow: 0px 0px 10px 0px rgb(5, 9, 20);
        div  {
          transform: translateX(0%);
        }
        p {
          transform: scale(1.05);
        }
        p:nth-child(4) {
          transform: scale(1.0);
          opacity: 1;
        }
      }
      #myProjectsBlock-secondImage {
        position: relative;
        margin-left: 15%;
        background-image: linear-gradient(rgba(0, 0, 0, .6), rgba(0, 0, 0, .6)), url('@/assets/Weather.png');
        background-size: cover;
        p:nth-child(2) {
          right: 5%;
        }
        p:nth-child(3) {
          right: 5%;
        }
        p:nth-child(4) {
          left: -50px;
        }
      }
    }
    a:last-child {
      margin-top: 100px;
      margin-left: 10%;
    }
  }

  @media(max-width: 450px) {
    .myProjectsBlock {
      height: 700px;
      h2 {
        margin-top: 50px;
        height: auto;
        font-size: 34px;
      }
      a {
        width: 80%;
        height: 200px;
        margin-top: 50px; 
        div {
          p {
            margin-top: calc(35% - 10px);
            font-size: 28px;
          }
          p:nth-child(3) {
            margin-top: calc(35% + 30px);
            font-size: 22px;
          }
          p:nth-child(4) {
            display: none;
          }
        }
        #myProjectsBlock-secondImage {
          margin-left: 0px;
          p:nth-child(3) {
            text-align: right;
          }
        }
      }
      a:last-child {
        margin-top: 50px;
      }
    }
  }

  @media(min-width: 600px) and (max-width: 1100px) {
    .myProjectsBlock {
      height: 1000px;
      h2 {
        height: 100px;
        font-size: 34px;
      }
      a {
        height: 300px;
        div {
          p {
            margin-top: calc(34% - 10px);
            font-size: 32px;
          }
          p:nth-child(3) {
            margin-top: calc(35% + 20px);
            font-size: 26px;
          }
          p:nth-child(4) {
            display: none;
          }
        }
      }
    }
  }

  @media(min-width: 1800px) {
    .myProjectsBlock {
      height: 1770px;
      h2 {
        font-size: 52px;
      }
      a {
        height: 650px;
        div {
          p {
            margin-top: calc(30% - 10px);
            font-size: 52px;
          }
          p:nth-child(3) {
            margin-top: calc(30% + 60px);
            font-size: 38px;
          }
        }
      }
    }
  }
</style>
