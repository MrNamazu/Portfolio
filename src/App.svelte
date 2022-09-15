<script>
  import Navigation from './lib/components/menu.svelte'
  import Logo from './lib/components/logo.svelte'
  import Smalllogo from './lib/components/smallLogo.svelte'
  import Noisebg from './lib/components/noisebg.svelte'
  import Hero from './lib/components/hero.svelte'
  import Projects from './lib/components/projects.svelte'
  import { Splide, SplideSlide } from '@splidejs/svelte-splide';
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  import '@splidejs/svelte-splide/css/sea-green';

  AOS.init();

  let loading = false;
  let progress = 0;

/*   const increaseProgress = async () => {
		setInterval(() => {
			if (progress === 100) {
				loading = false;
        return;
			} else {
				progress++;
			}
		}, 20);
	};
  increaseProgress(); */

</script>
<Noisebg />
{#if loading}
<div class="loading">
  <Smalllogo />
  <p>Loading...</p>
  <p>{progress}</p>
</div>
{:else}
<div class="pageWrapper">
  <div class="pageContainer">
    <div class="header">
      <div class="headerWrapper">
        <Logo />
        <Navigation />
      </div>
    </div>
    <div class="contentWrapper">
      <Hero />
      <Projects />
      <div class="split" />
        <ul class="footerNav">
          <li><a href="/">Impressum</a></li>
          <li><a href="/">Partner & Friends</a></li>
          <li><a href="/">Twitter</a></li>
          <li><a href="/">Discord</a></li>
        </ul>
      <div class="split" />
      <p class="footerText">Web-development <span style="color: #FFF !important;">with love ♥</span></p>
      <div class="split" />
      <p class="footerText">© 2022 • PHILSTACK</p>
    </div>
  </div>
</div>
{/if}
<style>
.loading {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
@media (min-width: 800px) {
  .pageWrapper {
    width: 100%;
    display: flex;
    justify-content: center;
  }
  .pageContainer {
    width: 80%;
  }
}
.pageContainer {
  position: relative;
  height: 100%;
}
.pageWrapper {
  width: 100%;
  height: 100%;
  position: relative;
}
.header {
  position: absolute;
  width: 100%;
  height: 70px;
  padding: 20px;
  z-index: 22;
}

.headerWrapper {
  height: 70px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.contentWrapper {
  padding: 120px 20px 20px 20px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.content {
  background-color: #FFF;
  height: 200px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.split {
  height: 1px;
  width: 100%;
  background-color: rgba(255,255,255,0.3);
}
.footerText {
  font-weight: 600;
  text-transform: uppercase;
  font-size: 11px;
  text-align: center;
  color: rgba(255,255,255,0.6);
  margin: 0;
}
.footerNav {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.footerNav li a {
  color: #FFF;
  font-weight: 600;
  text-decoration: none;
  font-size: 11px;
  cursor: pointer;
}
</style>
