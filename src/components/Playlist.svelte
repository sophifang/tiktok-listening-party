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
            <div class='playedRecently'> <PlayedRecently {cooldowns}/> </div>       
        </div>
    </div>
</main>
  
<style>
    .song{
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top: 8px;
    }

    .upNext{
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top: 8px;
    }

    .playedRecently{
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top: 8px;
    }

    .playlist{
        background: rgb(190,84,100);
        background: linear-gradient(-187deg, #CD5063 0%, #532E5A 21%);
        border-radius: 12px;
        width: 301px;
        height: 608px;
    }

    .phone{
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>