<script>
	let elapsed = 53;
	let duration = 262;

    function format(time) {
		let minutes = Math.floor(time / 60);
		let seconds = Math.floor(time % 60);

		return `${minutes}:${seconds < 10 ? `0${seconds}` : seconds}`;
	}
</script>

<main>
    <div class="slider">
        <div class="progress" style="--progress: {elapsed / duration}%"></div>
    </div>  
    <div class="times" style="margin-top: 1px">
        <span>{format(elapsed)}</span>
        <span style="text-align: right">{format(duration)}</span>
    </div>
</main>

<style>
    .slider {
        margin-top: 8px;
		flex: 1;
        width: 310px;
		height: 0.3em;
		background: var(--bg-2);
		border-radius: 0.5em;
		overflow: hidden;
        background-color: #BFBFBF;
	}

    .progress {
		width: calc(100 * var(--progress));
		height: 100%;
		background: var(--bg-3);
        background-color: #F6F3F7;
	}

    .times{
        font-size: 10px;
        color: #F6F3F7;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 500;
        font-style: normal;
        font-variation-settings: "slnt" 0;

        display: grid;
		grid-template-columns: 1fr 1fr;
    }
</style>