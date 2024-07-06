<script>
	import UpNext from './UpNext.svelte';
    export let playlist;

	/////////  Song Numbering  ////////////
	// let counter = 0;
	// let increment = () =>{
	// 	counter++
	// 	console.log(counter)
	// 	return counter;
	// }

	// button click handler 
	let visible = {};
	for (let elem of playlist) {
		visible[elem[0]] = false;
	}; 

	//boosting alg
	async function boosted(song){
		for (let elem of playlist) {
			if (elem[0] == song) {
				elem[3] += 1;
			}
		} 
  	};


	
</script>

<main>
	<img class = "pop-up" src = "Boosts.png" alt = "pop-up screen" />

	<div class="icon-buttons">
		{#each playlist as song}
			{#if visible[song[0]] === true}
				<label>
					<input class="to-boost" type="image" src="boost_ clicked.png" alt="song icon" on:click={() => boosted(song[0])}>
				</label>

					{:else}
				 	<label>
						<input type="image" src="song-icon.png" class= "song-icon" alt="song-icon" on:click={() => (visible[song[0]] = true)}/>
				 	</label>
			{/if}
			
		{/each}
	</div>

	
</main>

<style>
	
	.pop-up{
		width: 313.5px;
        transform: translate(-98%, 81%);
		border-radius: 25px;
	}


	.icon-buttons{
		width: 300px;
		height: 250px;
        transform: translate( -100%, -10%);
	}

	.song-icon{
		scale: 0.7;
		/* padding: 1px; */
	}

	.to-boost{
		scale: 0.7;
	}

	/* .song-num{
		font-size: 10px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
		width: 10px;
		transform: translate( 10%, 20%);

	} */


	
</style>