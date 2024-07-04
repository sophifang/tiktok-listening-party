<script>
    import AudioPlayer from "./AudioPlayer.svelte";
    export let song;
</script>

<main>
    <section>
        <img style="scale: 1.2; margin-left: 7px" src="ttpd.png"/>
        <div>
            Now Playing:  
            <span style="font-weight: 600">{song[0]}</span>
            <br/>
            <span style="font-size:10px; font-weight:400; color:#F6F3F7">{song[1]}</span>
             <br/>
            <AudioPlayer/>
        </div>
    </section>
</main>

<style>
    section{
        font-size: 15px;
        color: #F6F3F7;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;

		width: 384px;
        height: 78px;
		display: grid;
		grid-template-columns: 1fr 4fr;
        margin-top: 12px;
	}

    .center {
		text-align: left;
        display: flex;
        flex-flow: column;
        justify-content: center;
	}


</style>
