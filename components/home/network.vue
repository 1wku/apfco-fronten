<template>
  <div class="container network">
    <img src="images/network-map.png" alt="mạng lưới apfco" />
    <div class="network__content">
      <h2 class="xxl-semibold">{{ $t("home__network-title") }}</h2>
      <span class="divider-decor"></span>
      <p class="network__des xl-normal">
        {{ $t("home__network-content") }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeNetwork',
}
</script>

<style lang="scss" scoped>
@import '~/assets/styles/colors.scss';
@import '~/assets/styles/mixins/responsive';

.network {
  position: relative;

  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 32px 0;

  &::before {
    content: '';
    position: absolute;
    height: 100%;
    width: 100vw;
    z-index: -99;

    background: url('/images/network-decor.png'),
      linear-gradient(11.23deg, #86c146 7.11%, #00a44e 100.22%);
    background-repeat: no-repeat;
    background-size: contain;
  }

  &>img {
    width: 50%;

    @include mobile {
      position: absolute;
      opacity: 0.2;
      filter: drop-shadow(2px 4px 6px black) brightness(0.7);
      width: 60%;

      height: 100%;

      object-fit: contain;
    }
  }

  &__content {
    padding-left: 2rem;
    color: #fff;

    &>* {
      margin-bottom: 2rem;
    }

    &>h2 {}

    & .divider-decor {
      width: 2rem;
      height: 0.25rem;
      display: block;

      background: $apfco-red;
      border-radius: 2px;
    }

    &__des {
      width: 48rem;
      text-align: center;
    }
  }

  @include mobile {
    padding: 3rem 1rem;

    &__content {
      padding: 0;
    }
  }
}
</style>
