<script>
  import { Splide,SplideSlide,SplideTrack } from '@splidejs/svelte-splide';
  import '@splidejs/svelte-splide/css/core';
</script>

<h2 style="margin: 0;">My Projects</h2>
<p style="font-size: 12px; margin: 0 0 8px 0;">Projects and websites I´ve created or been part of the team.</p>
<div id="projects">
<Splide hasTrack={ false } aria-label="..." options={{gap: "10px", fixedWidth: "300px",perMove: 1, arrows: false, pagination: false, wheel: true,}} >
  <SplideTrack>
    <SplideSlide>
      <div class="container">
        <img src="assets/img/xivdb.png" alt="XIVDB" />
      </div>
    </SplideSlide>
    <SplideSlide>
      <div class="container">
        <img src="assets/img/trio.png" alt="Landkautz" />
      </div>
    </SplideSlide>
    <SplideSlide>
      <div class="container">
        <img src="assets/img/trio.png" alt="TrioState" />
      </div>
    </SplideSlide>
    <SplideSlide>
      <div class="container">
        <img src="assets/img/trio.png" alt="Kreativ Werkstatt" />
      </div>
    </SplideSlide>
    <SplideSlide>
      <div class="container">
        <img src="assets/img/trio.png" alt="Side Projects" />
      </div>
    </SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
    <SplideSlide><div class="container">Coming Soon</div></SplideSlide>
  </SplideTrack>
</Splide>
</div>

<style>
  #projects > :global(.splide) {
    padding: 0 !important;
  }
  .container {
    width: 100%;
    height: 200px;
    background-color: rgba(0,0,0,0.4);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Integral CF;
    font-size: 11px;
    color: rgba(255,255,255,0.4);
    transition: .3s all;
    cursor: pointer;
  }
  .container:hover {
    background-color: rgba(0,0,0,0.7);
    transition: .3s all;
  }
  .container img {
    width: 100%;
    height: 100%;
    opacity: 0.6;
    transition: .3s all;
    border: 0px solid #FFF;
    object-fit: cover;
  }
  .container img:hover {
    border: 0px solid #FFF;
    opacity: 1;
    transition: .3s all;
  }
  h2 {
    text-transform: uppercase;
    color: #FFF;
    font-size: 18px;
  }
</style>