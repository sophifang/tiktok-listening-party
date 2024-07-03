<script>
  import Playlist from './Playlist.svelte';

  let song = ["So Long, London", "The Tortured Poets Department", "ttpd.png", 262000]
  let playlist = [
    ["Fortnight", "The Tortured Poets Department", "ttpd.png", 0, 31],
    ["Cruel Summer", "Lover", "lover.png", 0, 128], 
    ["Shake It Off", "1989 (Taylor’s Version)", "1989.png", 0, 75],
    ["Paper Rings", "Lover", "lover.png", 0, 48], 
    ["Blank Space", "1989 (Taylor’s Version)", "1989.png", 0, 45],
    ["Down Bad", "The Tortured Poets Department", "ttpd.png", 0, 61],
    ["Lover", "Lover", "lover.png", 0, 189]
  ];  

  let cooldowns = [
    ["Fortnight(feat. Post Malone)", "The Tortured Poets Department", "ttpd.png", 6],
    ["Welcome to New York", "1989 (Taylor’s Version)", "1989.png", 15]
  ];  

  let boost = {
    "Fortnight": 1,
    "Cruel Summer": 1,
    "Shake It Off": 1,
    "Paper Rings": 1,
    "Blank Space": 1,
    "Down Bad": 1,
    "Lover": 1,
  };  

  async function boosted(){
    playlist[Math.floor(Math.random() * 6)][3] += 1
  };

</script>

<main>
  <div class="boost-playlist">
    <div class="button-wrapper">
      <button on:click={boosted}>Boost Random Song</button>
    </div>
    <Playlist {playlist} {cooldowns} {song} {boost}/>  
  </div>
</main>

<style>
  .boost-playlist{
    display: grid;
		grid-template-columns: 1fr 1fr;
  }

  .button-wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
