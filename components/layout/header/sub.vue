<template>
  <div class="subHeader xs-normal padding">
    <p>Công Ty Cổ Phần Nông Sản Thực Phẩm Quảng Ngãi</p>
    <p></p>
    <div class="subHeader-left">
      <client-only>
        <select @change="onChange($event)" class="lang">
          <option value="vi">VI</option>
          <option value="en">EN</option>
        </select>
      </client-only>
      <div class="work">
        <svg
          width="14"
          height="14"
          viewBox="0 0 14 14"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M11.6668 12.8333H10.5002V11.6666C10.5002 11.2025 10.3158 10.7573 9.9876 10.4291C9.65941 10.101 9.21429 9.91658 8.75016 9.91658H5.25016C4.78603 9.91658 4.34091 10.101 4.01273 10.4291C3.68454 10.7573 3.50016 11.2025 3.50016 11.6666V12.8333H2.3335V11.6666C2.3335 10.893 2.64079 10.1512 3.18777 9.60419C3.73475 9.05721 4.47661 8.74992 5.25016 8.74992H8.75016C9.52371 8.74992 10.2656 9.05721 10.8126 9.60419C11.3595 10.1512 11.6668 10.893 11.6668 11.6666V12.8333ZM7.00016 7.58325C6.54054 7.58325 6.08541 7.49272 5.66077 7.31683C5.23613 7.14094 4.85029 6.88313 4.52529 6.55813C4.20028 6.23312 3.94248 5.84728 3.76658 5.42264C3.59069 4.998 3.50016 4.54288 3.50016 4.08325C3.50016 3.62363 3.59069 3.1685 3.76658 2.74386C3.94248 2.31922 4.20028 1.93338 4.52529 1.60838C4.85029 1.28337 5.23613 1.02556 5.66077 0.849674C6.08541 0.673782 6.54054 0.583252 7.00016 0.583252C7.92842 0.583252 8.81866 0.952001 9.47504 1.60838C10.1314 2.26476 10.5002 3.15499 10.5002 4.08325C10.5002 5.01151 10.1314 5.90175 9.47504 6.55813C8.81866 7.2145 7.92842 7.58325 7.00016 7.58325ZM7.00016 6.41658C7.619 6.41658 8.21249 6.17075 8.65008 5.73317C9.08766 5.29558 9.3335 4.70209 9.3335 4.08325C9.3335 3.46441 9.08766 2.87092 8.65008 2.43334C8.21249 1.99575 7.619 1.74992 7.00016 1.74992C6.38132 1.74992 5.78783 1.99575 5.35025 2.43334C4.91266 2.87092 4.66683 3.46441 4.66683 4.08325C4.66683 4.70209 4.91266 5.29558 5.35025 5.73317C5.78783 6.17075 6.38132 6.41658 7.00016 6.41658Z"
            fill="white"
          />
        </svg>
        <a href="http://apfco.com.vn/htmx/basic/login/login.aspx">{{
          $t('work')
        }}</a>
      </div>
      <a class="linktoold" target="_blank" href="http://apfco.com.vn/?v=o"> Website cũ</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LayoutHeaderSub',
  methods: {
    onChange(e) {
      this.$router.push(this.switchLocalePath(e.target.value))
    },
  },
}
</script>

<style lang="scss" scoped>
@import '~/assets/styles/colors.scss';
@import '~/assets/styles/mixins/responsive';

.subHeader {
  width: fill;
  height: 1.875rem;

  color: #fff;
  background: $apfco-green;

  display: flex;
  justify-content: space-between;
  align-items: center;

  &-left {
    display: flex;
    justify-content: end;
    align-items: center;
  }

  @include mobile {
    display: none;
  }
}

.lang {
  margin-right: 1rem;
}

.work {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-right: 1rem;
}

.linktoold {
  font-weight: 500;
  padding: 0 1rem;
  height: 1.875rem;

  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid $apfco-green;
  transition: all 0.3s ease-in;

  &:hover {

    background-color: #fff;
    color: $apfco-green;
  }
}
</style>
