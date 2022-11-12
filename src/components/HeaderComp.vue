<template>
  <div class="nav">
    <img src="@/assets/Group-1.png" title="BKorobka" alt="BKorobka">
    <span>
      <p>
        <a href="#About">Обо мне</a>
      </p>
      <p>
        <a href="#Projects">Мои проекты</a>
      </p>
      <p>
        <a href="#Contacts">Контакты</a>
      </p>
    </span>
  </div>
</template>

<script>

export default {
  name: 'HeaderComp',
  data() {
    return {
    }
  },
  components: {
  },
}
</script>


<style scoped lang="scss">

  .nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-left: 9.75%;
    width: 81.25%;
    height: 70px;
    color: white;
    img {
      margin-right: 1%;
      width: 5.5%;
      height: 55px;
      background-size: cover;
    }
    span {
      display: flex;
      justify-content: space-between;
      width: 40%;
      font-family: 'Open Sans', sans-serif;
      color: rgb(208, 208, 208);
      p {
        width: 30%;
        height: 35px;
        font-size: 20px;
        line-height: 35px;
        text-align: center;
        a {
          color: rgb(208, 208, 208);
          text-decoration: none;
          transition: 150ms ease;
          cursor: pointer;
        }
        a:hover {
          color: white;
          border-style: solid;
          border-color:  white;
          border-width: 0px 0px 3px 0px;
        }
      }
      p:nth-child(1){
        width: 25%;
      }
    }
  }

  @media(max-width: 450px){
    .nav {
      flex-direction: column;
      margin-left: 10%;
      width: 85%;
      height: 150px;
      img {
        margin-top: 10px;
        margin-right: 6%;
        width: 20%;
      }
      span {
        margin-top: 30px;
        width: 100%;
        height: 70px;
        p {
          width: 30%;
          height: 70px;
          font-size: 16px;
          line-height: 20px;
        }
      }
    }
  }

  @media(min-width: 600px) and (max-width: 1100px) {
    .nav {
      img {
        width: 7.5%;
      }
      span {
        width: 50%;
        p {
          line-height: 20px;
          font-size: 16px;
        }
      }
    }
  }

  @media(min-width: 1800px) {
    .nav {
      height: 120px;
      img {
        width: 6.5%;
        height: 85px;
      }
      span {
        width: 45%;
        p {
          font-size: 30px;
        }
      }
    }
  }
</style>