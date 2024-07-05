<script>
    import CurrentSong from './CurrentSong.svelte';
    import UpNext from './UpNext.svelte';
    import PlayedRecently from './PlayedRecently.svelte';
    export let playlist, cooldowns, song;
  </script>
  
<main>
    <div class='phone'>
        <div class='playlist'>
            <div class='song'> <CurrentSong {song}/> </div>
            <div class='upNext'> <UpNext {playlist}/> </div>
            <div class='playedRecently'> <PlayedRecently {playlist} {cooldowns}/> </div>       
        </div>
    </div>
</main>
  
<style>
    .song{
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top: 12px;
    }

    .upNext{
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top: 12px;
    }

    .playedRecently{
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top: 12px;
    }

    .playlist{
        scale: 0.7;
        width: 430px;
        background: rgb(100,99,97);
        background: linear-gradient(-184deg, rgba(100,99,97,1) 0%, rgba(58,58,55,1) 21%);
        border-radius: 12px;

    }

    .phone{
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>