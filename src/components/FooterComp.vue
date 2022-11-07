<template>
  <footer id="Contacts">
    <img src="@/assets/Group-1.png" title="BKorobka" alt="BKorobka">
    <span>
      <p><a href="https://vk.com/k0r0bochk4">Вконтакте</a></p>
      <p><a href="https://github.com/RoastedPikachu">Github</a></p>
      <p><a href="https://t.me/KorobkaBoris">Телеграм</a></p>
    </span>
    <p>&#169; Boris Karabut 2022</p>
  </footer>
</template>

<script>
export default {
  name: 'FooterComp',
  data() {
    return {
      
    }
  }
}
</script>

<style scoped lang="scss">
  footer {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 70px;
    width: 100%;
    height: 250px;
    background-color: #1c1d25; 
    img {
      margin-top: -30px;
      width: 80px; 
      height: 80px;
    }
    span {
      display: flex;
      justify-content: center;
      width: 100%;
      p {
        margin-left: 80px;
        font-size: 22px;
        font-family: 'Open Sans', sans-serif;
        text-align: center;
        a {
          color: white;
          text-decoration: none;
          transition: 150ms ease;
        }
        a:hover {
          color: white;
          border-style: solid;
          border-color:  white;
          border-width: 0px 0px 3px 0px;
        }
      } 
      p:first-child {
        margin-left: 0px;
      }
    }
    p {
      color: white;
      font-size: 16px;
      font-family: 'Lora', serif;
    }
  }

  @media(max-width: 450px) {
    footer {
      height: 200px;
      img {
        width: 60px;
        height: 60px;
      }
      span {
        justify-content: center;
        flex-wrap: wrap;
        p {
          margin-left: 0px;
          width: 40%;
          font-size: 18px;
        }
      }
      p {
        font-size: 12px;
      }
    }
  }

  @media(min-width: 600px) and (max-width: 1100px) {
    footer {
      height: 225px;
      img {
        width: 70px;
        height: 70px;
      }
      span {
        p {
          font-size: 20px;
        }
      }
      p {
        font-size: 14px;
      }
    }
  }

  @media(min-width: 1800px) {
    footer {
      height: 300px;
      img {
        width: 100px;
        height: 100px;
      }
      span {
        p {
          font-size: 30px;
        }
      }
      p {
        font-size: 24px;
      }
    }
  }
</style>
