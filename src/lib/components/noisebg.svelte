<script>

</script>


<div class="redBG"></div>
<div class="blackBG"></div>
<!-- <div class="testBG"></div> -->
<div class="noiseBG"></div>
<div class="bg"></div>
<style>
.bg {
  background-color: black;
}
.blackBG {
  position: fixed;
  pointer-events: none;
  z-index: 1;
  width: 100%;
  height: 100%;
  background: radial-gradient(
    circle,
    rgba(0, 0, 0, 0) 64%,
    rgba(0, 0, 0, 0.5) 100%
  );
}
.redBG {
  position: fixed;
  pointer-events: none;
  z-index: -1;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    180deg,
    rgba(182, 22, 22, 1) 0%,
    rgba(213, 36, 36, 1) 28%,
    rgb(8, 8, 8) 96%
  );
}
  .noiseBG {
    z-index: 20;
    pointer-events: none;
    position: fixed;
    overflow: hidden;
    top: -50%;
    left: -50%;
    right: -50%;
    bottom: -50%;
    width: 200%;
    height: 200vh;
    background: transparent url(http://assets.iceable.com/img/noise-transparent.png) repeat 0 0;
    animation: bg-animation .3s infinite;
    opacity: .7;
    visibility: visible;
    z-index: 2000;
  }
  @keyframes bg-animation {
    0% { transform: translate(0,0) }
    10% { transform: translate(-5%,-5%) }
    20% { transform: translate(-10%,5%) }
    30% { transform: translate(5%,-10%) }
    40% { transform: translate(-5%,15%) }
    50% { transform: translate(-10%,5%) }
    60% { transform: translate(15%,0) }
    70% { transform: translate(0,10%) }
    80% { transform: translate(-15%,0) }
    90% { transform: translate(10%,5%) }
    100% { transform: translate(5%,0) }
}
  
</style>