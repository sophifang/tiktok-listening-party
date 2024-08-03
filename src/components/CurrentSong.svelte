<script>
    import AudioPlayer from "./AudioPlayer.svelte";
    export let song;
</script>

<main>
    <section>
        <img src={song[2]} width="48px" height="48px"/>
        <div class="info">
            Now Playing:  
            <span style="font-weight: 600">{song[0]}</span>
            <br/>
            <span style="font-size:10px; font-weight:300; color:#F6F3F7">{song[1]}</span>
             <br/>
            <AudioPlayer/>
        </div>
    </section>
</main>

<style>
    section{
        font-size: 10px;
        color: #F6F3F7;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 300;
        font-style: normal;
        font-variation-settings: "slnt" 0;

		width: 270px;
        height: 50px;
		display: grid;
		grid-template-columns: 1fr 4fr;
        margin-top: 8px;
	}

    .info{
        margin: auto;
    }

</style>
