<script>
	import UpNext from './UpNext.svelte';
	import PlayedRecently from './PlayedRecently.svelte';
	export let cooldowns, playlist;


	let pos = {};

	// button click handler 
	let visible = {};
	let clicked = {};
	for (let elem of playlist) {
		visible[elem[0]], clicked[elem[0]] = false;
	}; 

	//boosts a song
	async function boosted(song){
    for (let elem of playlist) {
      if (elem[0] == song) {
        elem[3] += 1;
				//set to unclicked
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
				<div class ="boost-icon">
					<input class="to-boost" type="image" src="Boost-clicked.png" alt="Boost Button" on:click={() => boosted(entry[0])}>
					<img class="song-cover" src={entry[2]} alt="song-record-cover">
          <!-- <div class="song-title">Queue: {pos[0]}</div> -->
					<div class="song-title">Queue: </div>
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
    
    <!-- Cooldown Song Icon -->
		{#each cooldowns as entry}
			<div class ="cooldown-icon">
				<input type="image" src="cooldown-{entry[0]}.png" id="timed-out" alt="song-icon" />
				<div class="song-title">{entry[0]}</div>
			</div>
		{/each}

		<!-- Current Song Icon -->
		<div class ="cooldown-icon">
			<input type="image" src="current-song-icon.png" id="timed-out" alt="song-icon" />
			<div class="song-title">Street Symphony</div>
		</div>

	</div>
  
</main>

<style>
  
	.cooldown-icon{
    display: inline;
    align-items: center;
    justify-content: center;
    text-align: center;
		width: 70%;
		height: 70%;
		margin: auto;
	}

	.boost-icon{
		display: inline;
    align-items: center;
    justify-content: center;
    text-align: center;
		width: 70%;
		height: 70%;
		margin: auto;
	}

	.icon{
    display: inline;
    align-items: center;
    justify-content: center;
    text-align: center;
		width: 70%;
		height: 70%;
		margin: auto;
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
        grid-template-columns: 1fr 1fr 1fr 1fr;
		grid-auto-rows: 1fr;
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
	}

	
    .song-title{
        font-size: 5px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        transform: translate( 0px, -32px);
		margin: auto;
		width: 90%;
    }

	.icon:hover{
		background-color: rgba(255, 255, 255, 0.176);
		opacity: 0.7;
		border-radius: 6px;
	}

	#timed-out{
		background-color: #454542;
		border-radius: 6px;
	}
	
</style>