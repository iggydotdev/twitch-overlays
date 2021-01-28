<script>
    export let w;
    export let h;
    const styles = `width: ${w-48}px; height: ${h}px`;
</script>

<div class='webcam-container' style={styles}></div>



<style>
   .webcam-container {
       
       border: 4px solid orangered;
       padding: 20px;
       margin-top: 20px;
   }
</style>