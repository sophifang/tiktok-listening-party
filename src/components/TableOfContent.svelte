<script>
    export let menuSelected;
</script>

<main>
    <aside class:menuSelected>
        <div id="menu-container">
            <ul id="menu">
                <h3 id="menu-heading">
                    Table of Contents
                </h3>
                <li>
                    <a href="#joining-a-listening-party" id="jump-marker">I. Joining a Listening Party</a>
                </li>
                <div id="subheading">
                    <li>
                        <a href="#tiktok-live" id="jump-marker">A. TikTok LIVE</a>
                    </li>
                    <li>
                        <a href="#for-you-page" id="jump-marker">B. For You Page</a>                    
                    </li>
                    <li>
                        <a href="#music-feed" id="jump-marker">C. Music Feed</a>
                    </li>
                    <li>
                        <a href="#artist-profile" id="jump-marker">D. Artist Profile</a>                    
                    </li>
                </div>
                <li>
                    <a href="#listening-party" id="jump-marker">II. Listening Party</a>                    
                </li>
                <div id="subheading">
                    <li>
                        <a href="#hosting-a-listening-party" id="jump-marker">A. Hosting a Listening Party</a>
                    </li>
                    <li>
                        <a href="#main-screen" id="jump-marker">B. Main Screen</a>                    
                    </li>
                    <li>
                        <a href="#song-information" id="jump-marker">C. Song Information</a>
                    <li>
                        <a href="#collaborative-playlist" id="jump-marker">D. Collaborative Playlist</a>                    
                    </li>
                </div>
                <li>
                    <a href="#reward-system" id="jump-marker">III. Reward System</a>
                </li>
                <div id="subheading">
                    <li>
                        <a href="#tokens" id="jump-marker">A. Tokens</a>
                    </li>
                    <li>
                        <a href="#listener-level" id="jump-marker">B. Listener Level</a>                    
                    </li>
                </div>
                <li>
                    <a href="#additional-features" id="jump-marker">IV. Additional Features</a>                    
                </li>
                <div id="subheading">
                    <li>
                        <a href="#rising-artist-spotlight" id="jump-marker">A. Rising Artist Spotlight</a>
                    </li>
                    <li>
                        <a href="#artist-community-goals" id="jump-marker">B. Artist Community Goals</a>                    
                    </li>
                </div>
                <li style="margin-top: 5px;">
                    <a href="#development-tools" id="jump-marker"> V. Development Tools</a>
                </li>
                <li>
                    <a href="#sources" id="jump-marker">VI. Sources</a>                    
                </li>
                <div id="subheading">
                    <li>
                        <a href="#research" id="jump-marker">A. Research</a>
                    </li>
                    <li>
                        <a href="#assets" id="jump-marker">B. Assets</a>                    
                    </li>
                </div>
            </ul>    
        </div>
    </aside>
    
</main>

<style>
    .menuSelected{
        right: 0px;
    }

    aside{
        background-color: white;
        position: fixed;
        top: 0;
        bottom: -1000px;
        right: -100%;
        z-index: 3;
        transition: right 0.3s ease-in-out;
        overflow-y: auto;
        height: 100%;
        box-shadow: 3px 6px 12px rgba(0, 0, 0, 0.25);
    }

    aside::after{
        content: '';
        display: block;
        height: 0%;
    }

    #menu-heading{
        text-align: center;
        margin: 0;
        padding-top: 80px;
        color: black;
    }

    #menu-container{
        margin: 0;
        padding: 0;

        font-size: 15px;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 300;
        font-style: normal;
        font-variation-settings: "slnt" 0;
        line-height: 40px;
        z-index: 0;
        height: 100%;
    }

    ul{
        margin: 0;
        padding-inline-start: 14px;
        padding-inline-end: 14px;
        padding-bottom: 20px;
        list-style: none;
    }

    #subheading{
        padding-left: 30px; 
        font-size: 13px;
        line-height: 25px;
    }
    
    li{
        width: 100%;
        padding-left: 4px;
        padding-right: 4px;
    }

    #jump-marker{
        color: black;
        text-decoration: none;
        padding: 4px;
    }

    #jump-marker:hover{
        color: #CA00F2;
        text-decoration: none;
        padding: 4px;
    }
</style>