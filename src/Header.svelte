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
        <p>{streamerName} </p> 
       {#if !!channel} 
        <span> @ </span>
        <p>{channel}</p>
        {/if}
    </div>
    
    <marquee direction="left" behavior="scroll" scrollamount="12" class='center-column'>
        <div>{title} - {description}</div>
    </marquee>

    <div class='right-column'>
        {#if !!topContributor}
            <div>Top Contributor: {topContributor}</div>
        {:else}
            <div> Be the first contributor! </div>
        {/if}
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
        margin: 0 20px;
        font-size: 16px;
        width: 100%;
    }

    .left-column {
        justify-content: flex-start;
    }
    .right-column {
        justify-content: flex-end;
    }

    p {
        margin: 0;
        padding: 0;
    }

    span {
        margin: 0 10px;
    }

</style>