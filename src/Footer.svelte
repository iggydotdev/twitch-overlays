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
            <div>f</div> <div>{facebook}</div>
        </div>
        
        <div class='youtube'>
            <div>ytb</div><div>{youtube}</div>
        </div>

        <div class='twitter'>
            <div>Twitter</div><div>{twitter}</div>
        </div>
    </div>

    <div class='now-playing'>
        <div>Now playing: </div> <div>{song}</div>
    </div>

    <div class='last-follower'>
        <div class='follow'>
            <div>Last follow:</div> <div>{follower}</div>
        </div>
    </div>
</footer>


<style>
   
    footer {
        height: 50px;
        display: flex;
        flex-flow: row nowrap;
        justify-content: space-between;
        align-items: center;
        color: white;
        background-color: royalblue;
        padding-left: 20px;
        padding-right: 20px;
        font-weight: normal;
        font-size: 10px;
        position: fixed;
        bottom: 0;
        width: calc(100% - 40px);
        padding-left: 20px;
        padding-right: 20px;
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




</style>