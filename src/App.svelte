<script>
  import { Router, Route } from "svelte-routing";
  import { root } from "./assets/js/paths.js";
  import Footer from "./components/Footer.svelte";
  import Header from "./components/Header.svelte";
  import Landing from "./pages/Landing.svelte";
  import Meta from "./pages/Meta.svelte";
</script>

<Router primary={false}>
  <Header />

  <div class="overlay  top--" />
  <div class="overlay  bottom--" />

  <div class="main">
    <Route path={root}>
      <Landing />
    </Route>

    <Route path="{root}/meta">
      <Meta />
    </Route>
  </div>

  <Footer />
</Router>

<style lang="scss">
  @import "./assets/scss/all.scss";

  .overlay {
    position: fixed;
    width: 100%;
    height: 15vh;
    z-index: $zi-overlay;

    &.top-- {
      top: 0;
      background: linear-gradient(white, 60%, rgba(255, 255, 255, 0));
    }

    &.bottom-- {
      bottom: 0;
      background: linear-gradient(rgba(255, 255, 255, 0), 40%, white);
    }
  }

  .main {
    @include wrapper;
    // padding: $wrapper-gutter 0;
    display: flex;
    flex-grow: 1;
    flex-direction: column;
    position: relative;
  }
</style>
