<script>
import { fly } from 'svelte/transition';
import { flip } from 'svelte/animate';

  let menuOpen = false;
  let scrollable = true;
	
	const wheel = (node, options) => {
		let { scrollable } = options;
		const handler = e => {
			if (!scrollable) e.preventDefault();
		};
		node.addEventListener('wheel', handler, { passive: false });
		return {
			update(options) {
				scrollable = options.scrollable;
			},
			destroy() {
				node.removeEventListener('wheel', handler, { passive: false });
			}
		};
  };

  const openMenu = () => {
    const body = document.querySelector('body')
    menuOpen = !menuOpen;
    AOS.refresh();
    if (!menuOpen) {
      scrollable = false;
    } else {
      scrollable = true;
    }
  }

</script>
<svelte:window use:wheel={{scrollable}} />
<style>
.menuIcon {
  background-color: #000;
  border-radius: 50%;
  height: 30px;
  width: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
.menuIcon i {
  color: #FFF;
  font-size: 12px;
  z-index: 21;
}
nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: rgba(182, 22, 22, 1);
  z-index: 20;
  height: 100%;
  padding: 120px 20px 20px 20px;
}
nav ul {
  list-style: none;
  margin: 0;
  padding: 20px;
}
nav ul li:not(:last-child) {
  margin-bottom: 20px;
}
nav ul li a {
  color: #FFF;
  font-size: 27px;
  text-transform: uppercase;
  text-decoration: none;
  font-weight: 800;
  letter-spacing: 5px;
}
nav ul li a {
  padding-left: 0px;
  transition: .2s all;
}
nav ul li a:hover {
  padding-left: 20px;
  transition: .2s all;
}
.split {
  height: 1px;
  width: calc(100% - 40px);
  background-color: rgba(0,0,0,1);
  margin: 40px 20px;
}
.subnav {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.subnav a {
  color: #FFF;
  text-decoration: none;
  font-weight: 600;
  font-size: 12px;
}
.subnav a:not(:last-child) {
  margin-bottom: 10px;
}
</style>


<div class="menuIcon" on:click={() => openMenu()}>
  <i class={menuOpen !== true ? 'fa-solid fa-bars' : 'fa-solid fa-xmark'}></i>
</div>
{#if menuOpen}
  <nav in:fly="{{ y: -1500, duration: 1000 }}" out:fly="{{ y: -1500, duration: 1000 }}">
    <ul class="mainMenu">
      <li data-aos="flip-up" data-aos-delay="1100" data-aos-duration="800"><a href="/" >Home</a></li>
      <li data-aos="flip-up" data-aos-delay="1200" data-aos-duration="800"><a href="/">My Projects</a></li>
      <li data-aos="flip-up" data-aos-delay="1300" data-aos-duration="800"><a href="/">About me</a></li>
      <li data-aos="flip-up" data-aos-delay="1400" data-aos-duration="800"><a href="/">Contact</a></li>
      <li data-aos="flip-up" data-aos-delay="1500" data-aos-duration="800"><a href="/">Impress</a></li>
    </ul>
    <div class="split" />
    <div class="subnav">
      <a href="/">Impressum</a>
      <a href="/">Datenschutz</a>
    </div>
    <div class="split" />
  </nav>

{/if}