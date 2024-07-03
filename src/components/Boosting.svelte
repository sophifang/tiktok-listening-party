<script>

    import Modal from './BoostingModal.svelte';

    let showModal = false;
    
</script>
  
<main>
    <div class = "container">
        <div class = "listening-screen">
            <img class = "background" src = "Listening Party - resized.png" />
        </div>

        <button class="boost-btn" on:click={() => (showModal = true)}> </button>

    </div>

    <Modal bind:showModal>
    </Modal>

  
</main>
  
<style>

    .container{
        margin-top: 50px;
        display: flex;
        justify-content: center;
    }

    .listening-screen .background {
        height: 700px;
        width: auto;
    }

    .container .boost-btn {
        position: absolute;
        top: 92%;
        left: 54%;
        transform: translate(-50%, -50%);
        -ms-transform: translate(-50%, -50%);
        background-color: transparent;
        color: white;
        border: none;
        cursor: pointer;
        height: 25px;
        width: 20px;
        border-radius: 10px;
        }
</style>

  