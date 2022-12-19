<template>
<div id="background-div">
    <div class="container">
  <div class="sliding-background">
  </div>
</div>
</div>
</template>

<script>
export default {

}
</script>

<style>


.container {
    position: relative;
    overflow:hidden;
}

.sliding-background {
    position: fixed;
    background: url('../assets/homepagebackground.jpg') repeat-x 0 / 100% auto;
    top: 1%;
    left: 0%;
    width: 100vw;
    height: 100vh;
    animation: slide 60s linear infinite;
}

@keyframes slide {
    0%{background-position: 0 0;}
	100%{background-position: 100vw 0;}
}


</style>