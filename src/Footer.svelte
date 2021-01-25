<script>
    export let facebook;
    export let youtube;
    export let twitter;
    export let song;
    export let follower;
</script>



<footer>
    <div class='social-media'>
        <div class='facebook'>
            <p>Facebook</p>
            <p>{facebook}</p>
        </div>
        
        <div class='youtube'>
            <p>Youtube</p>
            <p>{youtube}</p>
        </div>

        <div class='twitter'>
            <p>Twitter</p>
            <p>{twitter}</p>
        </div>
    </div>

    <div class='now-playing'>
        <p>Now playing: </p> 
        <marquee direction="left" behavior="scroll" scrollamount="12">{song}</marquee>
    </div>

    <div class='last-follower'>
        <div class='follow'>
            {#if !!follower}
                <p>Last follower</p> <p>{follower}</p>
            {:else}
                <p> Be the first follower!</p>
            {/if}
        </div>
    </div>
</footer>


<style>
   
    footer {
        display: flex;
        flex-flow: row nowrap;
        justify-content: space-between;
        align-items: center;
        color: white;
        background-color: royalblue;
        font-weight: normal;
        font-size: 16px;
        position: fixed;
        bottom: 0;
        width: calc(100% - 40px);
        padding: 20px;
    }

    .visually-hidden {
        clip: rect(0 0 0 0);
        clip-path: inset(50%);
        height: 1px;
        overflow: hidden;
        position: absolute;
        white-space: nowrap;
        width: 1px;
    }

    .social-media, 
    .now-playing,
    .last-follower {
        display: flex;
        flex-flow: row nowrap;
        justify-content: center;
        align-items: center;
    }

    .facebook, .youtube, .twitter, .follow {
        display: flex;
        flex-flow: column nowrap;
        justify-content: space-evenly;
        align-items: center;
        padding: 10px 20px;
    }

    marquee {
        margin-left: 10px;
    }

    p {
        margin-top: 0;
    }

    .facebook p:last-of-type, 
    .youtube p:last-of-type, 
    .twitter p:last-of-type, 
    .follow p:last-of-type {
        margin-bottom: 0;
    }




</style>