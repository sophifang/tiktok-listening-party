<script>
	import UpNext from './UpNext.svelte';
	import PlayedRecently from './PlayedRecently.svelte';
    import { treemapSlice } from 'd3';
	export let cooldowns;
    export let playlist;

	/////////  Song Numbering  ////////////
	// let counter = 0;
	// let increment = () =>{
	// 	counter++
	// 	console.log(counter)
	// 	return counter;
	// }

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
		{#each allSongs as song}
			{#if visible[song[0]] === true}


				<input class="to-boost" type="image" src="Boost-clicked.png" alt="Boost Button" on:click={() => boosted(song[0])}>
				<!-- <img class="song-cover" src={song[2]} alt="song-record-cover"> -->
				<!-- <div class="song-title">{song[0]}</div> -->

				{:else}
					<!-- <div>
						<input type="image" src="song-icon.png" class= "song-icon" alt="song-icon" on:click={() => (visible[song[0]] = true)}/>
					 <img class="song-cover" src={song[2]} alt="song-record-cover">
					</div> -->
				 	<input type="image" src="song-icon.png" class= "song-icon" alt="song-icon" on:click={() => (visible[song[0]] = true)}/>
					 <img class="song-cover" src={song[2]} alt="song-record-cover">
					 <!-- <div class="song-title">{song[0]}</div> -->
			{/if}
			
		{/each}
	</div>

	
</main>

<style>
	
	.pop-up{
		width: 313.5px;
        transform: translate(-98%, 84.5%);
		border-radius: 25px;
	}


	.icon-buttons{
		text-align: center;
		max-width: 300px;
		height: 250px;
        transform: translate( -100%, -6%);
	}
	
	input{
		max-width: 46px;
	}

	.song-icon{
		/* padding-left: 4%;
		padding-right: 4%;
		padding-top: 1.3%; */
	}

	.to-boost{
		/* padding-left: 4%;
		padding-right: 4%;
		padding-top: 1.3%; */
	}

	.song-cover{
		max-width:18px;
		border-radius: 100%;
		transform: translate( -275%, -190%);
		cursor: pointer;
	}

	/* .song-title{
		font-size: 5px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
		max-width: 50px;
		transform: translate( 200%, -500%);
	} */




	
</style>