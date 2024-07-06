<script>
    import Modal from './BoostingModal.svelte';
    export let playlist;

    let showModal = false;
    
</script>
  
<main>
    <div class = "phone-container">
        <img class = "listening-screen" src = "o_streamer_show_song.png" alt="phone screen"/>

        {#if showModal === true}
             <Modal {playlist}></Modal>
             {:else}
             <!-- <button class="boost-btn" on:click={() => (showModal = true)}> </button> -->
             <input type="image" src="waveform icon.png" class="boost-btn" alt="request icon" on:click={() => (showModal = true)}/>
        {/if}
        

    </div>

</main>
  
<style>
    .phone-container{
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .listening-screen{
        /* height: 532.46px; */
        height: 608px;
        width: 301px;
        border-radius: 12px;

    }

    .phone-container .boost-btn {
        transform: translate(-390%, 1070%);
        cursor: pointer;
        height: 25px;
        width: 25px;
    }
</style>

  