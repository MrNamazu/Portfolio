<script>
</script>

<style>
.heroContainer {
  width: 100%;
  height: 100vh;
  background-size: cover;
}
button {
  background: #fc5445;
  font-weight: 800;
  font-size: 12px;
  text-transform: uppercase;
  border: 0;
  padding: 10px 20px;
  color: #FFF;
  box-shadow: 0 0 3px #ff8859;
  font-family: "Montserrat";
  animation: animButton 2s infinite;
  cursor: pointer;
  transition: .3s all;
}
button:hover {
  background: #e83c2c;
  transform: scale(1.05) !important;
  transition: .3s all;
}
@keyframes animButton {
  0%, 100% {
    transform: scale(1.0);
  }
  50% {
    transform: scale(1.02)
  }
}
.heroContainer {
  display:flex;
  gap: 10px;
}
.left, .right {
  width: 50%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgba(0,0,0,0.1);
}
</style>

<div class="heroContainer">
<div class="left">

  <button>Contact me!</button>
</div>
<div class="right">
bildd
</div>

</div>