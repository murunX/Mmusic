<script>
  export let isNavbarVisible;
  import { createEventDispatcher } from "svelte";
  import { Songs } from "../../data/Songs";
  import { Users } from "../../data/User";
  let Song = Songs;
  let User = Users;
  const dispatch = createEventDispatcher();
</script>

<div
  class="header"
  style="width: {isNavbarVisible ? 'calc(100% - 240px)' : '100%'};"
>
  <div class="header-left">
    <button
      on:click={() => dispatch("toggleNavbar", "left")}
      tabindex="0"
      style="font-size: 24px;"
    >
      <i class="arrow left"></i>
    </button>
    <button
      on:click={() => dispatch("toggleNavbar", "right")}
      tabindex="0"
      style="font-size: 24px;"
    >
      <i class="arrow right"></i>
    </button>
  </div>
  <div class="header-right">
    <div class="current-song" style="background-image: url('{Song[0].Image}');">
      <div class="song-overlay">
        <div class="song-title">
          <p>{Song[0].title}</p>
        </div>
        <div class="play-button">
          <button id="play">
            <i class="fa-solid fa-play" style="color: #ffffff;"></i>
          </button>
        </div>
      </div>
    </div>
    <button id="notif">
      <i class="fa-regular fa-bell fa-lg" style="color: #E5E7EB;"></i>
    </button>
    <div class="user">
      <div class="user-left">
        <img src={User[0].Image} alt="" />
        <p>{User[0].name}</p>
      </div>
      <div class="user-right">
        <button>
          <i class="arrow down"></i>
        </button>
      </div>
    </div>
  </div>
</div>
