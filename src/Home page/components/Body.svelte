<script>
  import { Banners } from "../../data/Banners";
  import { Musics } from "../../data/Musics";
  let banner = Banners[0];
  let music = Musics;
  console.log(music);
</script>

<div class="content">
  <div class="main-content">
    <div class="banner" style="background-image: url('{banner.image}');"></div>
    <div class="songs">
      <h1>New hot</h1>
      <hr />
      <div class="song-card">
        {#each music.slice(0, 5) as music1}
          <div class="song-names">
            <img src={music1.Image} alt="" />
            <span>{music1.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Шинээр нэмэгдсэн бүтээлүүд</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
        <div>
          <p>Бүгд үзэх</p>
        </div>
      </div>
      <hr />
      <div class="song-card">
        {#each music.slice(5, 10) as music2}
          <div class="song-names">
            <img src={music2.Image} alt="" />
            <span>{music2.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Шинээр нэмэгдсэн бүтээлч</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
        <div>
          <p>Бүгд үзэх</p>
        </div>
      </div>
      <hr />
      <div class="song-card">
        {#each music.slice(5, 10) as music3}
          <div class="song-names">
            <img src={music3.Image} alt="" style="border-radius:100%" />
            <span>{music3.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Шинээр нэмэгдсэн хамтрал уран бүтээлчид</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
        <div>
          <p>Бүгд үзэх</p>
        </div>
      </div>
      <hr />
      <div class="song-card">
        {#each music.slice(10, 14) as music}
          <div class="song-names-long">
            <img src={music.Image} alt="" />
            <span>{music.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Санал болгох</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
        <div>
          <p>Бүгд үзэх</p>
        </div>
      </div>
      <hr />
      <div class="song-card">
        {#each music.slice(14, 20) as music3}
          <div
            class="song-names-suggest"
            style="background-color: {music3.color};"
          >
            <img src={music3.Image} alt="" />
            <span>{music3.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Mood mix</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
      </div>
      <hr />
      <div class="song-card">
        {#each music.slice(5, 10) as music3}
          <div class="song-names">
            <img src={music3.Image} alt="" />
            <span>{music3.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Сонгосон жанр</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
        <div>
          <p>Бүгд үзэх</p>
        </div>
      </div>
      <hr />
      <div class="song-card">
        {#each music.slice(5, 10) as music3}
          <div class="song-names">
            <img src={music3.Image} alt="" style="border-radius:100%" />
            <span>{music3.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Mmusic mix</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
      </div>
      <hr />
      <div class="song-card">
        {#each music.slice(5, 10) as music3}
          <div class="song-names">
            <img src={music3.Image} alt="" />
            <span>{music3.title}</span>
          </div>
        {/each}
        <hr />
        {#each music.slice(5, 10) as music3}
          <div class="song-names">
            <img src={music3.Image} alt="" />
            <span>{music3.title}</span>
          </div>
        {/each}
      </div>
    </div>
    <div class="songs">
      <div class="songs-title">
        <div class="songs-category">
          <h1>Өөр дуу сонсож үзэхүү?</h1>
          <p>Таны дагасан уран бүтээлчдээс тулгуурласан миксүүд</p>
        </div>
        <div>
          <p>Бүгд үзэх</p>
        </div>
      </div>
      <hr />
      <div class="song-card" style="margin-bottom:98px">
        {#each music.slice(0, 6) as music3}
          <div class="song-names-tall">
            <img src={music3.Image} alt="" />
            <p title={music3.name}>{music3.name}</p>
            <span>{music3.title}</span>
          </div>
        {/each}
        {#each music.slice(0, 6) as music3}
          <div class="song-names-tall">
            <img src={music3.Image} alt="" />
            <p title={music3.name}>{music3.name}</p>
            <span>{music3.title}</span>
          </div>
        {/each}
      </div>
    </div>
  </div>
</div>
