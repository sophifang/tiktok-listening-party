<script>
    let showBoost = false;
	
</script>


    {#if showBoost === true}
        <img class = "to-boost" src = "boost_ clicked.png" alt = "boost pop-up" />
        <button class= "boost-button"> </button>  
        {:else}
        <button class="song-icon" on:click={() => (showBoost = true)}> </button>
    {/if}



<style>

	.song-icon{
		padding: 20px;
		margin: 14px;
		background-color: transparent;
        color: transparent;
        border: none;
        cursor: pointer;
	}

    .to-boost{
        width: 65px;
        transform: translate(5%, 44%);   
	}

    .boost-button{
        width: 65px;
        height: 15px;
        transform: translate(-95%, 215%);   
        background-color: transparent;
        color: transparent;
        border: none;
        border-radius: 10px;
        cursor: pointer;
	}

    .boost-button:hover{
        width: 65px;
        height: 15px;
        transform: translate(-95%, 215%);   
        background-color: rgba(255, 255, 255, 0.123);
        color: transparent;
        border: none;
        border-radius: 10px;
        cursor: pointer;
	}


	
</style>