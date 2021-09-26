<div class="container footer">
  <div class="container  row-right--  footer-inner">LÉFROST</div>
</div>

<style lang="scss">
  @import "../assets/scss/all.scss";

  /* --- Footer --- */

  .footer {
    // opacity: 0;
    z-index: $zi-header;
    font-size: 16px;
    height: 40px;
    border-top: 1px solid $black;
  }

  .footer-inner {
    @include wrapper;
  }

  @media (min-width: $bp-lg) {
    .footer {
      font-size: 20px;
      height: 60px;
    }
  }
</style>
