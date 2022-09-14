<script>
  import Navigation from './lib/components/menu.svelte'
  import Logo from './lib/components/logo.svelte'
  import Noisebg from './lib/components/noisebg.svelte'
  import AOS from 'aos';
  import 'aos/dist/aos.css';

  AOS.init();
</script>
<Noisebg />
<div class="pageWrapper">
  <div class="pageContainer">
    <div class="header">
      <div class="headerWrapper">
        <Logo />
        <Navigation />
      </div>
    </div>
    <div class="contentWrapper">
      <div class="content"
      data-aos="flip-up">
        Lorem Ipsum
      </div>
    </div>
  </div>
</div>

<style>
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
  height: 100%;
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
}
.content {
  background-color: #FFF;
  height: 200px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
