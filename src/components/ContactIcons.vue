<template>
  <div class="contactIcons">
    <p><a href="https://github.com/RoastedPikachu"><i class="fa-brands fa-github"></i></a></p>
    <p><a href="https://t.me/KorobkaBoris"><i class="fa-brands fa-telegram"></i></a></p>
    <p><a href="https://vk.com/k0r0bochk4"><i class="fa-brands fa-vk"></i></a></p>
  </div>
</template>

<script>
export default {
  name: 'ContactIcons',
  data() {
    return {

    }
  }
}
</script>

<style scoped lang="scss">
  .contactIcons {
    position: absolute;
    display: flex;
    flex-direction: column;
    margin-top: 20%;
    right: 10px;
    width: 50px;
    height: 220px;
    z-index: 10;
    p {
      width: 100%;
      height: 60px;
      text-align: center;
      font-size: 36px;
      a {
        color: #898b98;
        transition: 200ms ease;
      }
    }
    p:hover {
      a {
        color: white;
      }
    }
  }

  @media(max-width: 475px) {
    .contactIcons {
      display: none;
    }
  }

  @media(min-width: 550px) and (max-width: 1100px) {
    .contactIcons {
      margin-top: 22%;
    }
  }

  @media(min-width: 1800px) {
    .contactIcons {
      margin-top: 12%;
      p {
        height: 80px;
        font-size: 52px;
      }
    }
  }

</style>
