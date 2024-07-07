<script>
  import Playlist from './Playlist.svelte';
  import ListeningParty from './ListeningParty.svelte';
  import Boosting from './Boosting.svelte';


  let song = ["Endless Sun", "Eternal Summer Skies", "album_cover/endless_sun.png", 0]
  let playlist = [
    ["The Place We Used To Go", "Whimsical Memories", "album_cover/the_place_we_used_to_go.png", 0],
    ["Rise Again", "Phoenix Heart", "album_cover/rise_again.png", 0], 
    ["Dancing Through the Tears", "Melancholy Moves", "album_cover/dancing_through_the_tears.png", 0],
    ["Moonlight Whispers", "Starlit Secrets", "album_cover/moonlight_whispers.png", 0], 
    ["Heart in Your Hands", "City Lights Romance", "album_cover/heart_in_your_hands.png", 0],
    ["Votes for Her", "Voices of Change", "album_cover/votes_for_her.png", 0],
    ["Street Symphony", "Urban Rhythms", "album_cover/street_symphony.png", 0],
    ["Last Dance", "Final Twirl", "album_cover/last_dance.png", 0],
    ["Too Many Hours", "Coal Mine Blues", "album_cover/too_many_hours.png", 0]
  ];  
  

  let cooldowns = [
    ["Dreamers", "Golden Childhood", "album_cover/dreamers.png", 6],
    ["Heart Beats Faster", "Electric Nights", "album_cover/heart_beats_faster.png", 15]
  ];  

  async function reset(){
    for(let i=0; i < playlist.length; i++){
      playlist[i][3] = 0;
    }
  };
</script>

<main>
  <!-- Navigation Bar -->
  <nav>
    <div class="container">
      <ul>
        <h1 class="menu-heading">
          TheJams
        </h1>
        <li style="padding: 1vw;">
          <a href="https://github.com/sophifang/tiktok-listening-party" target="_blank">
            <img 
              src="github-mark.png" 
              alt="GitHub Repo" 
              title="GitHub Repo" 
              width="35px"
            />
          </a>
        </li>
        <li>
          <a href="https://www.figma.com/proto/WhRSRwaN7Rr8fHFvNbTqGn/Designs?node-id=444-2386&t=dZ8PawirI0kKnMej-0&scaling=scale-down&content-scaling=fixed&page-id=327%3A1404&starting-point-node-id=444%3A2386&show-proto-sidebar=1" target="_blank">
            <img 
              src="Figma-logo.png" 
              alt="Figma" 
              title="Figma Demo"
              width="32px"/>
          </a>
        </li>
      </ul>
    </div>
  </nav>
  <!-- Article -->
  <div class="page">
    <h1>
      Introducing TikTok’s newest listening party feature building artist/fan communities and enhancing music discovery
    </h1>

    <div class="authors">
      By Cristina De La Torre, Sophia Fang, Carmen Truong, and Kathleen Nguyen
      <div class="date">
        Jul 1, 2024
      </div>
    </div>
    
    <img class="promo" src="temp-img.png" alt="Promo"/>

    <p class="article">
      Last year, so and so artist something. And this is a big issue, many other artists are labeled one hit wonders. 
      Steve Lacy trying to get their fans to sing the non-viral second verse.Lorem ipsum dolor sit amet, consectetur 
      adipiscing elit. Nam sed ligula ac dui tempus luctus. Proin eu quam volutpat, blandit ligula sed, aliquam libero. 
      In dictum ante justo, a euismod elit ultrices at. Donec ac ante at nunc accumsan hendrerit. Etiam malesuada suscipit 
      vehicula. Nulla vel urna ut ligula ultrices rhoncus. Integer augue massa, porta at nisl at, egestas aliquet risus.
        Duis luctus ligula dolor, vitae pretium nisi mollis eu.
    </p>

    <p class="article">
      Mauris eget tempus felis. Nam blandit est mi, eget suscipit tellus porttitor eget. Vestibulum rhoncus orci sapien, 
      rutrum efficitur justo mattis vitae. Quisque tellus enim, malesuada sit amet tellus vitae, dignissim egestas leo. Vivamus
      pellentesque metus dolor, quis blandit erat venenatis vel. Orci varius natoque penatibus et magnis dis parturient montes,
        nascetur ridiculus mus. Nullam sit amet tortor ligula. Etiam a condimentum lorem, a tempus quam. Fusce auctor vestibulum
        purus id gravida. Maecenas consequat tortor imperdiet cursus gravida. Praesent finibus libero ut ipsum molestie, ac molestie nisl tempus.
          Nullam posuere condimentum enim quis faucibus. Nulla egestas fringilla nisl, ut scelerisque dui euismod et.

    </p>

    <p class="article">
      Nulla facilisi. Pellentesque bibendum lorem eget pellentesque aliquet. Ut non fermentum nulla. 
      Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aliquam luctus
        odio eu sagittis scelerisque. Nunc facilisis nisi eros, in fermentum metus lobortis quis. Praesent ac
        ullamcorper lectus, nec feugiat diam. Suspendisse potenti.

    </p>

    <!-- Playlist -->
    <div class="boost-playlist">
      <div class = "boost-listening">
        <Boosting {playlist} {cooldowns} /> 
      </div>

      <div class="playlist">
        <Playlist {playlist} {cooldowns} {song}/>  
      </div>
    </div>
    <div class="button-wrapper">
      <!-- <button on:click={boosted} style="margin-right: 10px">Boost Random Song</button> -->
      <button on:click={reset}>Reset</button>
    </div>

    <p class="article">
      Sed ac est risus. Nam congue massa at diam finibus semper. Ut ac diam ac mauris vulputate blandit. 
      Cras pellentesque nunc quam, quis maximus lacus fermentum quis. Vivamus eget iaculis odio, in blandit 
      ipsum. Proin gravida purus sed dolor vehicula fringilla. Nunc maximus tempus velit, id consequat turpis
        ullamcorper et. Nunc posuere libero nec ligula placerat aliquam. Donec imperdiet risus in ante euismod
        ultrices. Proin vestibulum lectus iaculis, congue enim eu, dapibus tortor.
    </p>

    <!-- Listening Party -->
    <ListeningParty />

    <p class="article" style="margin-bottom: 10vh">
      Sed ac est risus. Nam congue massa at diam finibus semper. Ut ac diam ac mauris vulputate blandit. 
      Cras pellentesque nunc quam, quis maximus lacus fermentum quis. Vivamus eget iaculis odio, in blandit 
      ipsum. Proin gravida purus sed dolor vehicula fringilla. Nunc maximus tempus velit, id consequat turpis
        ullamcorper et. Nunc posuere libero nec ligula placerat aliquam. Donec imperdiet risus in ante euismod
        ultrices. Proin vestibulum lectus iaculis, congue enim eu, dapibus tortor.
    </p>  

    <div id="footer">
      Try out our full demo in 
      <a href="https://www.figma.com/proto/WhRSRwaN7Rr8fHFvNbTqGn/Designs?node-id=444-2386&t=dZ8PawirI0kKnMej-0&scaling=scale-down&content-scaling=fixed&page-id=327%3A1404&starting-point-node-id=444%3A2386&show-proto-sidebar=1" target="_blank">Figma</a> 
      or check out this article's code in our 
      <a href="https://github.com/sophifang/tiktok-listening-party" target="_blank">GitHub repo</a>!
    </div>  
  </div>

</main>

<style>
  #footer {
    text-align: center;
    font-weight: 500;
    margin-bottom: 10vh;
  }

  .container{
    position: relative;
    width: 100%;
  }

  .promo{
    margin-top: 40px;
    width: 100%;
  }

  h1{
    font-size: 40px;
    margin-bottom: 10px;
  }

  .authors{
    font-size: 15px;
    display: inline;
    font-weight: 400;
  }

  .date{
    display: inline;
    font-size: 15px;
    color: #7D7D7D
  }

  nav {
    display: flex;
		border-bottom: 0.1px solid rgba(0, 0, 0, 0.3);
    position: fixed;
    background-color: #FFFFFF;
    top: 0;
    left: 0;
    right: 0;
    z-index: 10;
  }

  ul {
    display: flex;
    margin-top: 0px;
    margin-bottom: 0px;
    padding-left: 2.5vw;
    list-style: none;
    align-items: center;
    justify-content: center;
  }
  
  li{
    margin: auto;
    padding-right: 2.5vw;
  }

  .menu-heading{
    font-size: 40px;
    margin: 0px;
    width: 85vw;
  }

  .page{
    max-width: 800px;
    text-align: left;
    display: grid;
    align-items: center;
    justify-content: center;

    font-size: 18px;
    font-family: "Inter", sans-serif;
    font-optical-sizing: auto;
    font-weight: 300;
    font-style: normal;
    font-variation-settings: "slnt" 0;

    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;

    margin-right: auto;
    margin-left: auto;
    margin-top: 100px;
    padding-left: 16px;
    padding-right: 16px;
  }

  @media (min-width: 650px) {
    .boost-playlist{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: auto auto;
      grid-column-gap: 0px;
      grid-template-areas:
        'top-left-container top-right-container'
        'bottom-left-container bottom-right-container';
    }
  }
  
  .boost-listening{
    display: flex;
    align-items: center;
    justify-content: center;

  }

  .button-wrapper{
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>