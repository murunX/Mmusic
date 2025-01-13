<script>
  let logo = "images/Mmusic.png";
  import { Buttons } from "../../data/Buttons";
  import { Playlist } from "../../data/Playlist";

  let buttons = Buttons;
  let playlist = Playlist;
</script>

<div class="side">
  <div class="logo">
    <img src={logo} alt="" style="height: 35px; width: 97px;" />
  </div>
  <div class="nav">
    {#each buttons.slice(0, 2) as btn}
      <button class="nav-link">
        <img src={btn.icon} alt="" />
        <span>{btn.title}</span>
      </button>
    {/each}
  </div>
  <div class="sub">
    <p>Миний сан</p>
    {#each buttons.slice(2, 5) as btn}
      <button class="sub-link">
        <img src={btn.icon} alt="" />
        <span>{btn.title}</span>
      </button>
    {/each}
    <hr />
    {#each playlist as list}
      <button class="sub-link">
        <img src={list.playlistImage} alt="" />
        <p1>{list.title}</p1>
      </button>
    {/each}
  </div>
</div>
