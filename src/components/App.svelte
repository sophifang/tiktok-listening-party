<script>
  import Playlist from './Playlist.svelte';
  import ListeningParty from './ListeningParty.svelte';
  import Boosting from './Boosting.svelte';


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

  // Temporary functions for buttons
  async function boosted(){
    playlist[Math.floor(Math.random() * 6)][3] += 1;
  };

  async function reset(){
    for(let i=0; i < playlist.length; i++){
      playlist[i][3] = 0;
    }
  };
</script>

<main>
  <nav>
    <ul>
      <h1 class="menu-heading">
        TheJams
      </h1>
      <li>
        <a href="https://github.com/sophifang/tiktok-listening-party" target="_blank"><img src="github-mark.png" href="https://github.com/sophifang/tiktok-listening-party" width="40px"/></a>
      </li>
      <li>
        <a href="https://www.figma.com/proto/WhRSRwaN7Rr8fHFvNbTqGn/Designs?node-id=444-2386&t=dZ8PawirI0kKnMej-0&scaling=scale-down&content-scaling=fixed&page-id=327%3A1404&starting-point-node-id=444%3A2386&show-proto-sidebar=1" target="_blank"><img src="Figma-logo.png" width="70px"/></a>
      </li>
    </ul>
  </nav>

  <div class="page">
    <h1>
      Introducing TikTok’s newest listening party feature building artist/fan communities and enhancing music discovery
    </h1>

    <div class="authors">
      By Cristina De La Torre, Sophia Fang, Carmen Truong, and Kathleen Nguyen
      <div class="date">
        Jul 1, 2024
      </div>
      <br/>
    </div>
    
    <img src="temp-img.png"/>

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
        <Boosting /> 
      </div>

      <Playlist {playlist} {cooldowns} {song}/>  

      <div class="button-wrapper">
        <button on:click={boosted} style="margin-right: 10px">Boost Random Song</button>
        <button on:click={reset}>Reset</button>
      </div>
    </div>

    <p class="article">
      Sed ac est risus. Nam congue massa at diam finibus semper. Ut ac diam ac mauris vulputate blandit. 
      Cras pellentesque nunc quam, quis maximus lacus fermentum quis. Vivamus eget iaculis odio, in blandit 
      ipsum. Proin gravida purus sed dolor vehicula fringilla. Nunc maximus tempus velit, id consequat turpis
       ullamcorper et. Nunc posuere libero nec ligula placerat aliquam. Donec imperdiet risus in ante euismod
        ultrices. Proin vestibulum lectus iaculis, congue enim eu, dapibus tortor.
    </p>

    <ListeningParty />

    <p class="article">
      Sed ac est risus. Nam congue massa at diam finibus semper. Ut ac diam ac mauris vulputate blandit. 
      Cras pellentesque nunc quam, quis maximus lacus fermentum quis. Vivamus eget iaculis odio, in blandit 
      ipsum. Proin gravida purus sed dolor vehicula fringilla. Nunc maximus tempus velit, id consequat turpis
       ullamcorper et. Nunc posuere libero nec ligula placerat aliquam. Donec imperdiet risus in ante euismod
        ultrices. Proin vestibulum lectus iaculis, congue enim eu, dapibus tortor.
    </p>

</main>

<style>
  h1{
    width: 800px;
    font-size: 40px;
    margin-bottom: 10px;
  }

  .authors{
    font-size: 15px;
    display: inline;
    margin-bottom: 40px;
    font-weight: 400;
  }

  .date{
    display: inline;
    font-size: 15px;
    color: #7D7D7D
  }

  .article{
    width: 800px;
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
    margin-top: 10px;
    margin-bottom: 10px;
    list-style: none;
    align-items: center;
    justify-content: center;
  }
  
  li{
    margin-right: 20px;
  }

  .menu-heading{
    margin: 0px;
    width: 1200px;
    font-size: 40px;
  }

  .page{
    margin-top: 80px;
    text-align: left;
    display: grid;
    align-items: center;
    justify-content: center;

    font-size: 20px;
    font-family: "Inter", sans-serif;
    font-optical-sizing: auto;
    font-weight: 300;
    font-style: normal;
    font-variation-settings: "slnt" 0;
  }

  .boost-playlist{
    display: grid;
		grid-template-columns: 1fr 1fr;
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