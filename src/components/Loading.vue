<template>
  <div class="wrap d-flex justify-content-center align-items-center flex-column">
    <h3>ALBUM</h3>
    <div class="loadingio-spinner-eclipse-fkkyh1ob51s"><div class="ldio-aejol2nd7aw">
    <div></div>
    </div></div>
    <h4>Loading</h4>
  </div>
</template>

<script>
export default {
  name: 'Loading',
}
</script>

<style lang="scss" scoped>
  .wrap{
    height: 100vh;
    color: white;
  }
  @keyframes ldio-aejol2nd7aw {
  0% { transform: rotate(0deg) }
  50% { transform: rotate(180deg) }
  100% { transform: rotate(360deg) }
}
.ldio-aejol2nd7aw div {
  position: absolute;
  animation: ldio-aejol2nd7aw 1s linear infinite;
  width: 160px;
  height: 160px;
  top: 20px;
  left: 20px;
  border-radius: 50%;
  box-shadow: 0 4px 0 0 #e15b64;
  transform-origin: 80px 82px;
}
.loadingio-spinner-eclipse-fkkyh1ob51s {
  width: 200px;
  height: 200px;
  display: inline-block;
  overflow: hidden;
  background: #1e2d3b;
}
.ldio-aejol2nd7aw {
  width: 100%;
  height: 100%;
  position: relative;
  transform: translateZ(0) scale(1);
  backface-visibility: hidden;
  transform-origin: 0 0; /* see note above */
}
.ldio-aejol2nd7aw div { box-sizing: content-box; }
</style>
