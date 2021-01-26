<script>
    export let w;
    export let h;
    const styles = `width: ${w}; height: ${h}px`;
    console.log(w, h)
</script>

<div class='webcam-container' style={styles}></div>



<style>
   .webcam-container {
       border: 4px solid orangered;
   }
</style>