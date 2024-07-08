<script>
  import Playlist from './Playlist.svelte';
  import ListeningParty from './ListeningParty.svelte';
  import Boosting from './Boosting.svelte';


  let song = ["Street Symphony", "Urban Rhythms", "album_cover/street_symphony.png", 0]
  let playlist = [
    ["The Place We Used To Go", "Whimsical Memories", "album_cover/the_place_we_used_to_go.png", 0],
    ["Rise Again", "Phoenix Heart", "album_cover/rise_again.png", 0], 
    ["Dancing Through the Tears", "Melancholy Moves", "album_cover/dancing_through_the_tears.png", 0],
    ["Moonlight Whispers", "Starlit Secrets", "album_cover/moonlight_whispers.png", 0], 
    ["Endless Sun", "Eternal Summer Skies", "album_cover/endless_sun.png", 0],
    ["Votes for Her", "Voices of Change", "album_cover/votes_for_her.png", 0],
    ["Last Dance", "Final Twirl", "album_cover/last_dance.png", 0],
    ["Heart in Your Hands", "City Lights Romance", "album_cover/heart_in_your_hands.png", 0],
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
          <a href="https://www.figma.com/proto/WhRSRwaN7Rr8fHFvNbTqGn/Designs?node-id=939-2353&t=JFR1hpJbFzYzJUaT-1&scaling=scale-down&content-scaling=fixed&page-id=327%3A1404&starting-point-node-id=939%3A2353&show-proto-sidebar=1" target="_blank">
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
        Jul 7, 2024
      </div>
    </div>
    
    <img class="promo" src="music_discovery.png" alt="Promo"/>

    <div class="heading" id="problem-statement">
      I. Problem Statement
    </div>

    <p class="article" >
      When we look at TikTok’s current state of music discovery, there is a general concern that artists who go viral on TikTok 
      will be unable to obtain a consistent audience, ultimately becoming known as one-hit wonders. While increasing exposure 
      and going viral on TikTok is important, artists also have to ensure that their impact is meaningful to sustain their newfound
       success. So, how do we achieve this? Our team, The Jams, propose implementing a new listening party feature that builds on 
       top of TikTok’s current LIVE infrastructure. This new feature will bridge the gap between fans and artists by providing a 
       space to explore discography, new and old, in a fresh engaging way. Fans may chat with one another and earn cool rewards 
       which together work to build a stronger sense of community all while streaming. Artists may also make surprise appearances
        to interact with their audience and strengthen their artist-fan communities.
    </p>


    <div class="heading" id="development-tools">
      II. Development Tools
    </div>

    <p class="article" >
      We prioritized developing the UI design and user flow of our concept so 
      audiences can better understand our vision. We built our full demonstration in Figma, and assets used can be found in section 
      VI. Source below. Suno AI was also used to generate fake songs including titles, lyrics, and covers. In addition to our Figma 
      designs, we built our website showcasing our idea using Svelte, a front-end software framework. The website is 
      mainly written in JavaScript, HTML, and CSS.
    </p>


    <div class="heading">
      III. Joining a Listening Party
    </div>

    <p class="article">
      Users are given four unique options to navigate to a Listening Party, allowing the feature to be readily accessible.
    </p>

    <div class="subheading">
      A. TikTok LIVE
    </div>

    <p class="article">
      The first option is through the LIVE feature where users will be shown Listening Party streams among other TikTok LIVEs. 
      When the “Explore” icon is clicked, a “Music” tab will be included with only Listening Parties listed. This will help present 
      the new Listening Party feature to both current and new TikTok users, especially those already familiar with TikTok LIVE.
    </p>

    <div class="subheading">
      B. For You Page
    </div>

    <p class="article">
      The second option is through the For You Page where a Listening Party may suddenly appear after the user swipes(in the same 
      way TikTok LIVEs appear). This will also help make the new Listening Party feature known to both current and new TikTok users.
    </p>

    <div class="subheading">
      C. Music Feed
    </div>

    <p class="article">
      The third option is through a new Music feed found by clicking on “Music” at the head of the Home page. At the top of the Music 
      feed is the user’s artist following list. A purple ring around the artist’s icon indicates whether or not the artist is currently 
      hosting a Listening Party. This list is presented to encourage users to listen to more songs in an artist’s discography which will 
      strengthen the user’s connection with the artist. Furthermore, users may swipe down on the page to see previews of personalized 
      recommended Listening Parties, similar to the For You Page’s setup. Tapping on the preview will lead the user to the Listening 
      Party. Users may opt to filter their recommendations using tags below the user’s artist following list. The Music feed was 
      conceptualized to make the Listening Party feature more identifiable and accessible.
    </p>


    <div class="subheading">
      D. Artist Profile
    </div>

    <p class="article">
      Lastly, the fourth option is on the artist’s profile page. Like TikTok’s LIVE feature, the artist’s icon will be highlighted to 
      indicate that a Listening Party is being hosted. To differentiate between a LIVE and a Listening Party, a purple ring will appear 
      rather than the traditional red ring. This option will help fans identify when their favorite artists are hosting a Listening Party 
      or prompt new fans to check out the music of an artist they just discovered.
    </p>

    <div class="heading">
      IV. Listening Party
    </div>

    <p class="article">
      In a busy industry where artists want to grow their community and promote new music, artists are encouraged to reach a wider audience 
      and they can do so by utilizing a new feature within TikTok, a Listening Party. A Listening Party is a type of livestream where artists
       and their audience can gather to listen to and talk about the artist’s music together. 
    </p>

    <div class="subheading">
      A. Hosting a Listening Party(Artist POV)
    </div>

    <p class="article">
      Let’s start off the Listening Party from an artist’s perspective. Artists will have access to start Listening Parties as soon as 
      TikTok approves of their artist profile. To accommodate an artist’s schedule, artists are given the option to plan Listening Parties 
      whether or not they are able to be present. This allows artists to interact with fans and the artists themselves can experience what 
      their audience thinks of their music. When the artist is present, they can decide whether or not to have their video on. Music will 
      always be playing, so the artist can mute themselves whenever necessary or they can pause the music for a moment if the artist wants 
      to talk about the song. If an artist is not able to be present during their Listening Party, they can start the LIVE and then return 
      later to end the party. In the artist’s place of where their video would be, the current song will be displayed instead with three 
      lines of lyrics at a time. Even though the artist is not present, the feature is still beneficial to the artist as it will help 
      build their community where listeners can meet each other and bond over the artist’s music. Artists are given a default playlist 
      that TikTok will provide by taking a sample of the artist’s entire discography despite whether or not the songs have been uploaded to 
      their TikTok music. Artists can edit the default playlist that TikTok suggested or the artist can decide on a playlist themselves and 
      their community will be able to collaborate by boosting songs they want to be added to the queue. More details about the collaborative 
      playlist and boosting features will be discussed in the following sections. Specific features for Listening Parties from the artist’s 
      perspective include buttons such as +Host and Control. The +Host button gives artists the opportunity to invite artists they may or may 
      not know to co-host the Listening Party with them and listeners will be able to listen to music from all participating artists. From the 
      artist perspective, utilizing +Host encourages artists to grow their communities with other artists who may have the same goal. From the 
      user perspective, if artists utilize +Host then users will be introduced to new artists and new genres of music. The Control button allows 
      artists to take over the playlist queue if they want to make changes during their Listening Party.
    </p>

    <div class="subheading">
      B. The Main Screen
    </div>

    <p class="article">
      From the user’s perspective, there are many ways to get involved in a Listening Party. By default, users are presented with a main screen 
      containing the current song’s title, cover, and a few lines of the lyrics. Clicking on the lyrics will open a separate screen with the complete
       lyrics. At the top of the main screen, users will see an option to follow the artist, the song’s category ranking if applicable, the two top 
       listeners, the number of concurrent listeners, and the Explore button. At the bottom of the main screen, users can take advantage of the live 
       chat to send messages to the artist as well as chat with other listeners. The bottom also includes an assortment of buttons that will provide 
       users with more options(more information in the following sections).
    </p>

    <!-- Listening Party -->
    <div class="listeningparty">
      <ListeningParty />
    </div>

    <div class="subheading">
      C. Learning More about Songs
    </div>

    <p class="article">
      Since we want users to leave the Listening Party knowing new songs, we give them the option to learn more about the current song being played. 
      By tapping the Song button, users will have the ability to bookmark the current song(which is added to their bookmarked sounds on TikTok), add 
      the song to their connected music platform, learn which album the song is from, and observe the lyrics to the song in full. The Song button makes 
      it more convenient for users to learn and save the song, thus, creating a more lasting impact.
    </p>


    <div class="subheading">
      D. Collaborative Playlist
    </div>

    <p class="article">
      We recognize fans may want to participate in choosing songs to play so we implemented a collaborative playlist with a design intentionally similar 
      to the Gift system in Tiktok’s LIVE feature. New users who are already familiar with the Gift system will have little difficulty understanding the 
      new one. When the “Request” icon at the bottom of the page is tapped, users will be presented with an overlay showcasing clickable icons. Each icon, 
      also known as a Boost, includes a single song available in the playlist along with a price in both Coins and Tokens(more on this feature later). Coins 
      can be purchased by clicking the Recharge button, which is identical to the LIVE feature. When the Boosts are tapped and purchased, users will be able 
      to push the respective song forward in the playlist. To see the current playlist with live updates, users may tap on the top right icon of the overlay. 
      Since we still want to induce a diverse range of songs to be played, songs will be set on 15 minute cooldowns after being played. This collaborative 
      playlist promotes a stronger sense of community as well as gives an additional reason for users to stay and wait for their favorite songs to play. 
      A demo of the collaborative playlist is available below.
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
      <button on:click={reset} class="reset-button">Reset</button>
    </div>

    <div class="heading">
      V. Reward System
    </div>

    <div style="margin-top: 20px;" class="subheading">
      A. Tokens
    </div>

    <p class="article">
      To encourage users to listen to more songs, we introduce a new currency called the Token that can be earned during the Listening Party, rather 
      than purchased. Users will earn 20 Tokens for each completed song they listen to. Tokens can be used to purchase Boosts much like Coins, however, 
      the purchase rate will be 100x greater than Coins. For example, if a song can be boosted by 1 Coin, then it can also be boosted by 100 Tokens, in 
      which case the user will need to listen to 5 complete songs to gather enough Tokens. This system grants all users, whether or not they have the 
      means to purchase Coins, the ability to participate in the collaborative playlist. Users will be motivated to listen to more songs to earn Tokens, 
      thereby increasing content exposure and diversity. 
    </p>

    <div class="subheading">
      B. Listener Level
    </div>

    <p class="article">
      A level-up mechanic is added to reward loyal fans and recognize their participation in Listening Parties. Users will earn experience points 
      that increase their Listener level, similar to the Gift system established in TikTok’s LIVE feature. Users will be given badges based on 
      their Listener level that will appear by their name in the artist’s Listening Party comment section. Some badges may include a notification 
      announcing the fan’s achievement. This will incentivize fans to listen to songs under an artist’s discography that they may not have heard 
      otherwise, increasing content diversity and building a stronger fan-artist connection.
    </p>

    <div class="heading">
      VI. Additional Features
    </div>

    <div style="margin-top: 20px;" class="subheading">
      A. Rising Artist Spotlight
    </div>

    <p class="article">
      The Music feed includes a banner titled “Rising Artist Spotlight” for users to check out new artists. This banner will showcase a single 
      rising artist each week. Tapping this banner will open a popup with more information on the artist. It was important for us to include this 
      banner to not only propel discovery for users, but to also support up and coming artists.
    </p>

    <div class="subheading">
      B. Artist Community Goals
    </div>

    <p class="article">
      Artists may opt to display a community goal on their profile page for a limited time. This feature can be used to encourage album streams, 
      sales, presales, and pre-saves. Moreover, clicking on the community goal will provide more information about the artist and their goal. The 
      community goal gives fans a clear call-to-action with pressure to be completed under a deadline. As a result, fans will be more likely to 
      interact and achieve goals set by the artist. 
    </p>

    <div class="heading">
      VII. Sources
    </div>

    <div class="subheading">
      A. Research
    </div>

    <a href="https://www.pewresearch.org/internet/2024/02/22/how-u-s-adults-use-tiktok/">https://www.pewresearch.org/internet/2024/02/22/how-u-s-adults-use-tiktok/</a>
    <a href="https://luminatedata.com/wp-content/uploads/2022/08/Luminate_Entertainment_365_Final.pdf">https://luminatedata.com/wp-content/uploads/2022/08/Luminate_Entertainment_365_Final.pdf</a>
    <a href="https://www.midiaresearch.com/blog/music-discovery-in-2023-is-about-the-journey-not-the-moment ">https://www.midiaresearch.com/blog/music-discovery-in-2023-is-about-the-journey-not-the-moment</a>

    <div class="subheading">
      B. Assets
    </div>
  
    Photo by cottonbro studio: 
    <br/>
    <a href="https://www.pexels.com/photo/a-woman-holding-a-microphone-while-singing-5648355/">https://www.pewresearch.org/internet/2024/02/22/how-u-s-adults-use-tiktok/</a>
    <br/>
    Photo by Erik Mclean:
    <br/> 
    <a href="https://www.pexels.com/photo/woman-holding-pink-flowers-on-the-tree-8517921/">https://www.pexels.com/photo/woman-holding-pink-flowers-on-the-tree-8517921/</a>
    <br/>
    Photo by Clara Ngo from Pexels:
    <br/> 
    <a href="https://www.pexels.com/photo/back-view-of-a-woman-in-brown-dress-3866555/">https://www.pexels.com/photo/back-view-of-a-woman-in-brown-dress-3866555/</a>
    <br/>
    Photo by Godisable Jacob: 
    <br/>
    <a href="https://www.pexels.com/photo/photo-of-woman-wearing-yellow-floral-top-871495/">https://www.pexels.com/photo/photo-of-woman-wearing-yellow-floral-top-871495/</a>
    <br/>
    Photo by Rajaa Lemnari:
    <br/>
    <a href="https://www.pexels.com/photo/couple-together-on-desert-19968907/">https://www.pexels.com/photo/couple-together-on-desert-19968907/</a>
    <br/>
    AI-Generated Images by Suno AI

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
    margin-top: 10vh;
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
  }

  .article{
    margin-top: 10px;
    line-height: 30px;
  }

  .heading{
    font-size: 20px;
    margin-top: 40px;
    margin-bottom: 0px;
    font-weight: 600;
  }

  .subheading{
    margin-top: 25px;
    font-weight: 500;
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
      margin-top: 40px;

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
    padding-top: 10px;
  }

  .reset-button{
    color: white;
    background-color: #EC1254;
    border-radius: 8px;
    border: none;
    cursor: pointer;
    padding-top: 6px;
    padding-bottom: 6px;
    padding-left: 15px;
    padding-right: 15px;
  }

  .listeningparty {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 40px;
    margin-bottom: 40px;
  }
</style>
