<script>
    export let streamerName;
    export let channel;
    export let title;
    export let description;
    export let topContributor;
</script>



<header>
    <h1 class='visually-hidden'>Twitch Streaming overlay</h1>

    <div class='left-column'>
        <div>{streamerName}</div>
        <div>{channel}</div>
    </div>
    
    <div class='center-column'>
        <div>{title}</div>
        <div>{description}</div>
    </div>

    <div class='right-column'>
        <div>Top Contributor: {topContributor}</div>
    </div>
</header>


<style>
   
    header {
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
        top: 0;
        width: calc(100% - 40px);
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

    .left-column, 
    .right-column,
    .center-column {
        display: flex;
        flex-flow: row nowrap;
        justify-content: center;
        align-items: center;
    }




</style>