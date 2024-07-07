<script>
	import UpNext from './UpNext.svelte';
	import PlayedRecently from './PlayedRecently.svelte';
	export let cooldowns;
    export let playlist;


	let allSongs = playlist.concat(cooldowns);

	// button click handler 
	let visible = {};
	for (let elem of allSongs) {
		visible[elem[0]] = false;
	}; 

	//boosts a song
	async function boosted(song){
		for (let elem of allSongs) {
			if (elem[0] == song) {
				elem[3] += 1;
				visible[elem[0]] = false;
			}
		} 
  	};
	
</script>

<main>
	<img class = "pop-up" src = "Boosts.png" alt = "pop-up screen" />

	<div class="icon-buttons">
		{#each allSongs as entry}
			{#if visible[entry[0]] === true}
				<!-- To Boost Icon -->
				<div class ="icon">
					<input class="to-boost" type="image" src="Boost-clicked.png" alt="Boost Button" on:click={() => boosted(entry[0])}>
					<img class="song-cover" src={entry[2]} alt="song-record-cover">
				</div>


				{:else}
					<!-- Default Song Icon -->
					<div class ="icon">
						<input type="image" src="song-icon.png" class= "song-icon" alt="song-icon" on:click={() => (visible[entry[0]] = true)}/>
					 	<img class="song-cover" src={entry[2]} alt="song-record-cover">
						<div class="song-title">{entry[0]}</div>
					</div>
			{/if}	
		{/each}

		<div class ="icon">
			<input type="image" src="song-icon.png" id="current" alt="song-icon" />
			<img class="song-cover" id="current-overlaid" src="album_cover/street_symphony.png" alt="song-record-cover">
			<div class="song-title" id="current-overlaid">Street Symphony</div>
			
		</div>

	</div>

	
</main>

<style>

	.icon{
        display: inline;
        align-items: center;
        justify-content: center;
        text-align: center;
    }

    
    .pop-up{
        width: 313.5px;
        transform: translate(-98%, 84.5%);
        border-radius: 25px;
    }
    .icon-buttons{
        max-width: 300px;
        height: 250px;
        transform: translate( -100%, -3%);
        display: grid;
        grid-template-columns: auto auto auto auto;
    }
    
    input{
        max-width: 46px;
    }

    .song-cover{
        max-width: 18px;
        border-radius: 100%;
        transform: translate( -180%, 20%);
        cursor: pointer;
        position: absolute;
        z-index: 1;
	}

	
    .song-title{
        font-size: 6px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        max-width: 45px;
        text-align: center;
        transform: translate( 11px, -35px);
    }

	.song-icon:hover{
		background-color: rgba(255, 255, 255, 0.176);
		border-radius: 6px;
	}

	#current{
		filter: blur(0.8px);
		background-color: rgba(255, 255, 255, 0.176);
		border-radius: 6px;
	}

	#current-overlaid{
		filter: blur(0.4px);
	}


	
</style>