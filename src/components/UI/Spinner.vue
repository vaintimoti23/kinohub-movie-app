<template>
  <div class="spin">
    <div class="lds-ring">
      <div></div>
      <div></div>
      <div></div>
      <div></div>
    </div>
  </div>
</template>

<style scoped>

.spin {
  background-color: rgba(11, 15, 34, 0.93);
  z-index: 2;
  width: 100%;
  height: 100%;
  position: absolute;
  margin: 0 auto;
}

.lds-ring {
  display: inline-block;
  position: relative;
  width: 110px;
  height: 110px;
  top: 50%;
  left: 50%;
}
.lds-ring div {
  box-sizing: border-box;
  display: block;
  position: absolute;
  width: 64px;
  height: 64px;
  margin: 0;
  border: 8px solid #fff;
  border-radius: 50%;
  animation: lds-ring 1.2s cubic-bezier(0.5, 0, 0.5, 1) infinite;
  border-color: #fff transparent transparent transparent;
}
.lds-ring div:nth-child(1) {
  animation-delay: -0.45s;
}
.lds-ring div:nth-child(2) {
  animation-delay: -0.3s;
}
.lds-ring div:nth-child(3) {
  animation-delay: -0.15s;
}
@keyframes lds-ring {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@media only screen and (max-width: 500px) {
  .lds-ring div{
    left: -21%;
  }
}
</style>