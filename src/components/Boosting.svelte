<script>
    import Modal from './BoostingModal.svelte';

    let showModal = false;
    
</script>
  
<main>
    <div class = "phone-container">
        <img class = "listening-screen" src = "Listening Party - resized.png" alt="phone screen"/>

        {#if showModal === true}
             <Modal></Modal>
             {:else}
             <button class="boost-btn" on:click={() => (showModal = true)}> </button>
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
        position: absolute;
        top: 91.5%;
        left: 28.5%;
        transform: translate(-50%, -50%);
        -ms-transform: translate(-50%, -50%);
        background-color: transparent;
        color: transparent;
        border: none;
        cursor: pointer;
        height: 25px;
        width: 20px;
        border-radius: 10px;
    }

    .phone-container .boost-btn:hover {
        background-color: #ffffff28;
        color: white;
    }

    .phone-container .boost-btn {
        background-color: transparent;
        color: white;
    }
</style>

  