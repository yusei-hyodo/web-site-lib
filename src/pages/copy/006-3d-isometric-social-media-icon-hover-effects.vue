<template lang="pug">
  .body
    ul
      li
        a(href="#")
          span
          span
          span
          span
          span
            font-awesome-icon(:icon="['fab','facebook-f']")
      li
        a(href="#")
          span
          span
          span
          span
          span
            font-awesome-icon(:icon="['fab','twitter']")
      li
        a(href="#")
          span
          span
          span
          span
          span
            font-awesome-icon(:icon="['fab','whatsapp']")
      li
        a(href="#")
          span
          span
          span
          span
          span
            font-awesome-icon(:icon="['fab','linkedin-in']")
      li
        a(href="#")
          span
          span
          span
          span
          span
            font-awesome-icon(:icon="['fab','instagram']")
</template>

<script>
export default {
  head: {
    titleTemplate: '006-3d-isometric-social-media-icon-hover-effects',
  },
}
</script>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}
.body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: #222;
}

ul {
  position: relative;
  display: flex;
  transform-style: preserve-3d;
  transform: rotate(-25deg) skew(23deg);

  li {
    position: relative;
    list-style: none;
    width: 60px;
    height: 60px;
    margin: 0 10px;

    &:nth-child(1):hover span {
      background: #3b5999;
    }

    &:nth-child(2):hover span {
      background: #55acee;
    }

    &:nth-child(3):hover span {
      background: #25d366;
    }

    &:nth-child(4):hover span {
      background: #0077b5;
    }

    &:nth-child(5):hover span {
      background: #e4405f;
    }

    &::before {
      content: '';
      position: absolute;
      bottom: -10px;
      left: 0;
      width: 100%;
      height: 10px;
      background: #2a2a2a;
      transform-origin: top;
      transform: skewX(-41deg);
    }

    &::after {
      content: '';
      position: absolute;
      top: 0;
      left: -9px;
      width: 9px;
      height: 100%;
      background: #2a2a2a;
      transform-origin: right;
      transform: skewY(-49deg);
    }

    span {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      justify-content: center;
      align-items: center;
      background: #333;
      color: rgba(255, 255, 255, 0.2);
      font-size: 30px !important;
      transition: 0.2s;

      svg {
        position: absolute;
        left: 50%;
        height: 100%;
        transform: translate(-50%, 0);
      }
    }

    &:hover span {
      z-index: 1000;
      transition: 0.5s;
      color: #fff;
      box-shadow: -1px 1px 1px rgba(0, 0, 0, 0.05);

      &:nth-child(1) {
        transform: translate(0px, 0px);
        opacity: 0.2;
      }

      &:nth-child(2) {
        transform: translate(10px, -10px);
        opacity: 0.4;
      }

      &:nth-child(3) {
        transform: translate(20px, -20px);
        opacity: 0.6;
      }

      &:nth-child(4) {
        transform: translate(30px, -30px);
        opacity: 0.8;
      }

      &:nth-child(5) {
        transform: translate(40px, -40px);
        opacity: 1;
      }
    }
  }
}
</style>
