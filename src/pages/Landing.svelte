<script>
  import { Link } from "svelte-routing";
  import { root } from "../assets/js/paths.js";
</script>

<div class="container  col--  row-lg--  block">
  <!-- 1 -->
  <div class="container  col-lg--  col-right--  stretch--">
    <div class="container  col--  stretch--  col-right--">
      <div class="landing-name">LÉ</div>
      <div class="landing-subname">RYAN KOROH</div>
      <div class="landing-subname">OLLÉ FROST</div>
    </div>
  </div>

  <!-- 2 -->
  <div class="container  grow--  stretch--  row-centre--">
    <div class="container  col--  col-centre--  grow--  stretch--  landing-mid">
      <div class="landing-mid__overlay  top--" />
      <div class="landing-mid__overlay  bottom--" />
      <div class="landing-mid__section">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. In metus vulputate
        eu scelerisque felis imperdiet. Eu mi bibendum neque egestas congue.
        Convallis aenean et tortor at risus viverra adipiscing. Morbi quis
        commodo odio aenean sed adipiscing diam donec adipiscing. Blandit turpis
        cursus in hac habitasse platea dictumst. Ultrices in iaculis nunc sed
        augue lacus viverra vitae. Ut tortor pretium viverra suspendisse potenti
        nullam ac tortor. Lacus laoreet non curabitur gravida arcu ac tortor
        dignissim. Turpis massa sed elementum tempus egestas. Mollis aliquam ut
        porttitor leo a. Aliquam faucibus purus in massa tempor nec. Faucibus in
        ornare quam viverra orci. Tincidunt dui ut ornare lectus sit amet est.
        Ultrices in iaculis nunc sed augue lacus.
      </div>
      <div class="landing-mid__feature">
        <a href="https://github.com/ollefrost" target="_blank"
          ><u>Sayman Dowman</u></a
        >, a brilliant absurdist with an absurdly brilliant wit → <Link
          to="{root}meta"
          ><u class="landing-mid__feature-other">and other curations</u></Link
        >.
      </div>
      <div class="landing-mid__section">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. In metus vulputate
        eu scelerisque felis imperdiet. Eu mi bibendum neque egestas congue.
        Convallis aenean et tortor at risus viverra adipiscing. Morbi quis
        commodo odio aenean sed adipiscing diam donec adipiscing. Blandit turpis
        cursus in hac habitasse platea dictumst. Ultrices in iaculis nunc sed
        augue lacus viverra vitae. Ut tortor pretium viverra suspendisse potenti
        nullam ac tortor. Lacus laoreet non curabitur gravida arcu ac tortor
        dignissim. Turpis massa sed elementum tempus egestas. Mollis aliquam ut
        porttitor leo a. Aliquam faucibus purus in massa tempor nec. Faucibus in
        ornare quam viverra orci. Tincidunt dui ut ornare lectus sit amet est.
        Ultrices in iaculis nunc sed augue lacus.
      </div>
    </div>
  </div>
  <!-- 3 -->
  <div class="container  row-bottom--  col-lg--  stretch-- ">
    <div class="container  grow--" />
    <div class="container  row-top--">
      <div class="container  col--  landing-links">
        <div class="landing-header">→ Works</div>
        <Link to="{root}meta"><u>Fullstack development</u></Link>
        <Link to="{root}meta"><u>Content creation</u></Link>
        <Link to="{root}meta"><u>Graphic design</u></Link>
      </div>
      <div class="container  col--  landing-links">
        <div class="landing-header">→ Socials</div>
        <Link to="{root}meta"><u>Anilist</u></Link>
        <Link to="{root}meta"><u>Behance</u></Link>
        <Link to="{root}meta"><u>Dribbble</u></Link>
        <Link to="{root}meta"><u>Instagram</u></Link>
        <Link to="{root}meta"><u>Twitter</u></Link>
      </div>
    </div>
  </div>
</div>

<style lang="scss">
  @import "../assets/scss/all.scss";

  // ----- Mid

  .landing-mid {
    padding: 50px 0;
    position: relative;
    max-width: 250px;
  }

  .landing-mid__section {
    font-size: 12px;
    line-height: 1.5;
    text-transform: uppercase;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 5;
    -webkit-box-orient: vertical;
    color: rgba($black, 0.8);
  }

  .landing-mid__section,
  .landing-mid__feature {
    text-align: justify;
    text-justify: inter-word;
  }

  .landing-mid__feature {
    padding: 20px 0;
    font-size: 20px;
    min-width: 80px;
  }

  .landing-mid__overlay {
    position: absolute;
    display: flex;
    width: 100%;
    height: 150px;

    &.top-- {
      top: 0;
      background: linear-gradient($white, 60%, rgba($white, 0));
    }

    &.bottom-- {
      bottom: 0;
      background: linear-gradient(rgba($white, 0), 40%, $white);
    }
  }

  @media (min-width: $bp-lg) {
    .landing-mid {
      padding: 0 6vw;
      max-width: 300px;
    }

    .landing-mid__overlay {
      height: 300px;
    }

    .landing-mid__section {
      font-size: 18px;
      -webkit-line-clamp: 10;
    }

    .landing-mid__feature {
      font-size: 24px;
    }
  }

  // ----- Name

  .landing-name {
    font-size: 120px;
    margin-bottom: -0.08em;
  }

  .landing-subname {
    font-size: 18px;
  }

  @media (min-width: $bp-lg) {
    .landing-name {
      font-size: 200px;
    }

    .landing-subname {
      font-size: 30px;
    }
  }

  // ----- Links

  .landing-header {
    padding-bottom: 30px;
  }

  .landing-links {
    &:not(:last-child) {
      padding-right: 5vw;
    }

    u {
      white-space: nowrap;
      position: relative;
      left: 0;

      &:hover {
        left: 5px;
      }
    }
  }

  @media (min-width: $bp-lg) {
  }
</style>
