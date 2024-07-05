<script>
	import SongButton from './SongButton.svelte';

	
</script>

<main>
	<img class = "pop-up" src = "Boosts.png" alt = "pop-up screen" />

	<table class="icon-buttons">
		{#each Array(2) as row}
			<tr>
				{#each Array(3) as column}

					<SongButton></SongButton>

				{/each}
			</tr>
		{/each}
	</table>
	  
	
</main>

<style>
	tr{
		height: 40px;
	}
	.pop-up{
		width: 301px;
		position: absolute;
		top: 75%;
        left: 25.3%;
        transform: translate(-50%, -50%);
        -ms-transform: translate(-50%, -50%);
		border-radius: 12px;
	}

	.icon-buttons{
		width: 301px;
		position: absolute;
		top: 68%;
        left: 30%;
        transform: translate(-50%, -50%);
        -ms-transform: translate(-50%, -50%);
	}


	
</style>