<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container colorFooter">
     
      <div class="copyright">
        &copy; {{ year }}   
        <a href="https://resclick.com/" target="_blank">ResClick.com</a>
        all rights reserved.
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style>
.colorFooter{
  background: linear-gradient(60deg,  #0f6386,#24A1D5);
  }
</style>
