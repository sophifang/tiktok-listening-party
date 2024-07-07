<script>
    import Modal from './BoostingModal.svelte';
    export let playlist;
    export let cooldowns;
    
</script>
  

<div class = "phone-container">
    <img class = "listening-screen" src = "test.png" alt="phone screen"/>
    <Modal {playlist} {cooldowns}></Modal>
</div>

  
<style>
    .phone-container{
        display: flex;
        width: 301px;
        margin: 0px;
		padding: 0px;
    }

    .listening-screen{
        height: 608px;
        border-radius: 12px;
        margin: 0px;
		padding: 0px;

    }

</style>

  