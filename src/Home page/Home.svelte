<script>
  import Body from "./components/Body.svelte";
  import Header from "./components/Header.svelte";
  import Navbar from "./components/Navbar.svelte";
  import Player from "./components/Player.svelte";
  let isNavbarVisible = true;

  function handleToggleNavbar(direction) {
    if (direction === "left") {
      isNavbarVisible = false;
    } else if (direction === "right") {
      isNavbarVisible = true;
    }
  }
</script>

<div class="home">
  <div class="navbar {isNavbarVisible ? '' : 'sidebar-hidden'}">
    <Navbar />
  </div>

  <div class="main" style="margin-left: {isNavbarVisible ? '240px' : '0'};">
    <Header
      {isNavbarVisible}
      on:toggleNavbar={(event) => handleToggleNavbar(event.detail)}
    />
    <Body />
  </div>
  <Player />
</div>
