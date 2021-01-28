<script>
    import config from './config/index';
    import VSCode from './VSCode.svelte';
    import Chat from './Chat.svelte';
    import Webcam from './Webcam.svelte';

</script>

<section>
    <div class="left-column">
        <VSCode/>
    </div>
    <div class="right-column">
        <Chat w={config.chat.width} h={config.chat.height}/>
        <Webcam w={config.webcam.width} h={config.webcam.height} />
    </div>
</section>


<style>
section {
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    height: 90vh;
}

.left-column {
    width: calc(100% - 320px);
    height: calc(90vh - 50px);
    padding: 20px;
}
.right-column {
    width: 320px;
    display: flex;
    flex-flow: column nowrap;
    height: calc(90vh - 50px);
    padding: 20px;
    padding-left: 0;
}

</style>