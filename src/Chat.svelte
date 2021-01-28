<script>
    export let w;
    export let h;

    const styles = `width: ${w-48}px; height: ${h}px`;
</script>

<div class='chat-container' style={styles}></div>



<style>
   .chat-container {
        border: 4px solid orangered;
        padding: 20px;
   }
</style>