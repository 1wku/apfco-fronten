<template>
  <div class="aboutus container">
    <div class="aboutus__decor">
      <img src="https://b-f11-zpc.zdn.vn/4079694386589023876/4decdad14ce494bacdf5.jpg" alt="" />
    </div>
    <div class="aboutus__content">
      <h2 class="xxl-semibold">{{ $t("home__aboutus-title") }}</h2>
      <span></span>
      <p class="xl-normal">
        <img src="https://b-f11-zpc.zdn.vn/4079694386589023876/4decdad14ce494bacdf5.jpg" alt="" class="image-mobile" />
        {{ $t("home__aboutus-content") }}
      </p>
      <nuxt-link to="about-us">
       <common-button :value="$t('see_more')" />
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/styles/colors.scss';
@import '~/assets/styles/mixins/responsive';

.aboutus {
  position: relative;
  height: 680px;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;

  height: fit-content;
  padding: 10rem 0;

  @include mobile {
    padding: 0;
  }

  &::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);

    width: 100vw;
    height: 80%;
    z-index: -9;

    background: linear-gradient(180deg,
        #ffffff 11.46%,
        rgba(255, 255, 255, 0) 100%),
      url('/images/aboutus-bg.png');
    background-repeat: no-repeat;
    background-position: top right;
    background-size: cover;
  }

  &__decor {
    width: 50%;
    height: fill;

    &>img {
      height: 100%;
      width: 100%;
      object-fit: contain;
      max-height: 500px;
    }

    @include mobile {
      display: none;
    }
  }

  &__content {
    padding-left: 4rem;
    width: 50%;

    @include mobile {
      width: 100%;
      padding: 3rem 1rem;
    }

    &>* {
      margin-bottom: 2rem;
    }

    &>h2 {
      color: $apfco-green;
    }

    &>span {
      width: 2rem;
      height: 0.25rem;
      display: block;

      background: $apfco-red;
      border-radius: 2px;
    }

    &>p {
      color: #667085;
    }
  }
}

.image-mobile {
  width: 40%;
  float: right;
  padding: 1rem;
  display: none;

  @include mobile {
    display: block;
  }
}
</style>
