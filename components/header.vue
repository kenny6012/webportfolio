<template>
  <div class="main_header">
      <div class="header_d">
          <span class="cover_title">A Team Player</span>
          <br>
          <span class="cover_sub">who has worked with multi-cultural and diverse team and has holistic knowledge of software development and design.</span>

      </div>
      <div class="faded_black"></div>
  </div>
</template>

<script>
export default {
data() {
  return {
  }
},
components: {

},
created() {
},
computed: {
  
}
}
</script>

<style lang="scss">
.main_header{
  background-image: url("../assets/sample_cover.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
.header_d {
    z-index: 2;
}
.faded_black {
    background: #00000082;
    width: 100%;
    height: 300px;
    border-radius: 10px;
    position: relative;
    top: -302px;
    left: 0px;
}
</style>
