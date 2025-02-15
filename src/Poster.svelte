<script>
  export let src;
  let imgHidden = false;
</script>

<img
  {src}
  class="poster"
  alt="poster"
  on:error={() => (imgHidden = true)}
  style="display: {imgHidden ? 'none' : 'block'};"
/>

<style>
  .poster {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
</style>
