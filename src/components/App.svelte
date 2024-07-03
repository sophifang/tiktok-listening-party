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
    playlist[Math.floor(Math.random() * 6)][3] += 1;
  };

  async function reset(){
    for(let i=0; i < playlist.length; i++){
      playlist[i][3] = 0;
    }
  };

  let page = 0;
  function next() {
        page++;
  }
  function back() {
        page--;
  }

</script>

<main>
  <div class="boost-playlist">
    <div class="button-wrapper">
      <button on:click={boosted} style="margin-right: 10px">Boost Random Song</button>
      <button on:click={reset}>Reset</button>
    </div>
    <Playlist {playlist} {cooldowns} {song} {boost}/>  
  </div>

  {#if page === 0}
      <div class = "song">
          <h1>So Long, London</h1>
          <img src="album.png" width="200" /> <br>
          <button on:click={next}>Stopped trying to drill the safe <br> Thinkin, how much sad did you think I had<br>Did you think I had in me?</button>
      </div>
  {/if}

  {#if page === 1}
      <div class = "lyrics">
            <img src="album.png" width="100"/>
            <button on:click={back}><img src="left-arrow.png" width="10" /></button>
            <p>So Long, London <br> The Tortured Poets Department</p>
            <p>I saw in my mind fairy lights <br>
              through the mist <br>
              I kept calm and carried the <br>
              weight of the rift <br>
              Pulled him in tighter each time <br>
              he was drifting away <br>
              My spine split from carrying <br>
              us up the hill <br>
              Wet through my clothes, <br>
              weary bones caught the chill <br>
              I stopped trying to make him laugh <br>
              Stopped trying to drill the safe <br>
              Thinkin, how much sad did <br>
              you think I had <br>
              Did you think I had in me? <br>
              Oh, the tragedy ... <br>
              So long, London <br>
              You'll find someone ... <br>
              I didn't opt in to be your odd man out <br>
              I founded the club she's heard <br>
              great things about <br>
              I left all I knew, you left me at <br>
              the house by the Heath <br>
              I stopped CPR, after all it's no use <br>
              The spirit was gone, <br> 
              we would never come to <br>
              And I'm pissed off you let me give <br>
              you all that youth for free <br>
              For so long, London <br>
              Stitches undone <br>
              Two graves, one gun <br>
              I'll find someone ... <br>
              And you say I abandoned the ship <br>
              But I was going down with it <br>
              My white knuckle dying grip <br>
              Holding tight to your quiet <br>
              resentment and <br>
              My friends said it isn't right <br>
              to be scared <br>
              Every day of a love affair <br>
              Every breath feels like rarest air <br>
              When you're not sure if he <br>
              wants to be there <br>
              So how much sad did you think I had, <br>
              Did you think I had in me? <br>
              How much tragedy? <br>
              Just how low did you think I'd go? <br>
              Before I'd self-implode <br>
              Before I'd have to go be free <br>
              You swore that you loved me but <br>
              where were the clues? <br>
              I died on the altar waiting for the proof <br>
              You sacrificed us to the gods of <br>
              your bluest days <br>
              And I'm just getting color back <br>
              into my face <br>
              I'm just mad as hell cause I <br>
              loved this place <br>
              For so long, London <br>
              Had a good run <br>
              A moment of warm sun <br>
              But I'm not the one <br>
              So long, London <br>
              Stitches undone <br>
              Two graves, one gun <br>
              You'll find someone ... <br>
            </p>
      </div>
  {/if}
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
