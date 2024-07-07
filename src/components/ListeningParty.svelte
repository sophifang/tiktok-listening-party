<script>
    import AudioPlayer from './AudioPlayer.svelte';

    let comment = '';

    let page = 0;
    function next() {
        page++;
    }
    function back() {
        page--;
    }
</script>

<main>
    {#if page === 0}
        <div class = "first">
            <div class = "content">
                <img class="phone-container" src="background.png" alt="Phone"/>
                <p class="title">Street Symphony</p>
                <img src="album_cover/street_symphony.png" alt="Album cover" class="album-cover-home">
                <div class="click-lyrics" on:click={next}>
                    <span class="different-color"> Street symphony, surviving <br> </span>
                    <span class="different-color"> through the storm, <br> </span>
                    <span> Voices of the block, <br> </span>
                </div>
                <input bind:value={comment} class="comment-box" placeholder="Comment">
                <img src="tiktok_emoji.png" alt="Comment emoji" class="emoji">
                <img src="recharge_icon.png" alt="Recharge icon" class="recharge-icon">
                <p class="recharge-text">Recharge</p>
                <img src="request_icon.png" alt="Request icon" class="request-icon">
                <p class="request-text">Request</p>
                <img src="album_icon.png" alt="Album icon" class="album-icon">
                <p class="song-text">Song</p>
                <img src="share_icon.png" alt="Share icon" class="share-icon">
                <p class="share-text">Share</p>
            </div>
        </div>
    {/if}

    {#if page === 1}
        <div class="second">
            <div class="content">
                <img class="lyrics-background" src="lyrics_background.png" alt="Phone"/>
                <img src="album_cover/street_symphony.png" alt="Album cover" class="album-cover-lyrics">
                <div class="back-button" on:click={back}>
                    <img src="left_arrow.png" width="12"/>
                </div>
                <p class="now-playing">Now Playing: </p>
                <p class="song-name">Street Symphony</p> <br>
                <p class="album-name">Urban Rhythms</p>
                <p class="song-lyrics">
                    <span> Raw feel, I'm street poetry <br> </span>
                    <span> birthed from grime, <br> </span>
                    <span> Echoes of struggle, gotta <br> </span>
                    <span> climb, penny to a dime, <br> </span>
                    <span> Glocks pop, corner blocks, <br> </span>
                    <span> the soundtrack of pain, <br> </span>
                    <span> Chains shine, move swift, <br> </span>
                    <span> dodgin' puddles in the rain. <br> </span>
                    <span> Brick by brick, stack <br> </span>
                    <span> knowledge, stack loot, <br> </span>
                    <span> Whippin' rhymes in the booth, <br> </span>
                    <span> sharp as tailored suits, <br> </span>
                    <span> Swift moves, chess game, <br> </span>
                    <span> every piece in place, <br> </span>
                    <span> Mask on, task on, <br> </span>
                    <span> never catch a case. <br> </span>
                    <span> Hustle on, grind strong, <br> </span>
                    <span> till the break of dawn, <br> </span>
                    <span class="different-color"> Street symphony, surviving <br> </span>
                    <span class="different-color"> through the storm, <br> </span>
                    <span> Voices of the block, <br> </span>
                    <span> stories etched in stone, <br> </span>
                    <span> Gritty tales, hard knocks, <br> </span>
                    <span> made it on my own. <br> </span>
                    <span> Studio’s a sanctuary, <br> </span>
                    <span> church for lost souls, <br> </span>
                    <span> Beats bang, dreams hang, <br> </span>
                    <span> heavy on our goals, <br> </span>
                    <span> Hard times breed legends, <br> </span>
                    <span> started from the bottom, <br> </span>
                    <span> Rising from the dust, like <br> </span>
                    <span> a phoenix, we got ‘em. <br> </span>
                    <span> Crown tilted, heavy is the <br> </span>
                    <span> head that’s gotta wear it, <br> </span>
                    <span> Verses cut deep, true grit, <br> </span>
                    <span> can't compare it, <br> </span>
                    <span> Through the fire, wordsmith, <br> </span>
                    <span> spitting hot coal, <br> </span>
                    <span> Street preacher, living proof, <br> </span>
                    <span> dug out the soul. <br> </span>
                    <span> Hustle on, grind strong, <br> </span>
                    <span> till the break of dawn, <br> </span>
                    <span> Street symphony, surviving <br> </span>
                    <span> through the storm, <br> </span>
                    <span> Voices of the block, <br> </span>
                    <span> stories etched in stone, <br> </span>
                    <span> Gritty tales, hard knocks, <br> </span>
                    <span> made it on my own. <br> </span>
                </p>
                <div class ="song-length">
                    <AudioPlayer />
                </div>
            </div>
        </div>
    {/if}
</main>

<style>
    .phone-container {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        width: 301px;
        height: 608px;
        border-radius: 12px;
    }

    .lyrics-background {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        width: 301px;
        height: 608px;
        border-radius: 12px;
    }

    .content {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        width: 301px;
        height: 608px;
    }

    .title {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 15px;
        color: rgba(255,255,255,1);
        position: absolute;
        top: 145px;
    }

    .album-cover-home {
        position: absolute;
        top: 190px;
        width: 150px;
    }

    .click-lyrics {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 13px;
        color: rgba(48,27,48,1);
        position: absolute;
        bottom: 200px;
        padding: 6px;
        cursor: pointer;
    }

    .click-lyrics:hover {
        width: 220px;
        border-radius: 20px;
        background-color: rgba(45,25,54,0.2);
        box-sizing: border-box;
    }

    .different-color {
        color: rgba(255,255,255,1);
    }

    .comment-box {
        font-family: 'Inter', sans-serif;
        font-size: 14px;
        position: absolute;
        bottom: 15px;
        left: 15px;
        width: 120px;
        padding: 6px;
        border: none;
        border-radius: 15px;
        background-color: rgba(22,22,34,0.2);
        box-sizing: border-box;
    }

    .comment-box::placeholder {
        font-family: 'Inter', sans-serif;
        font-size: 12px;
        position: absolute;
        bottom: 8px;
        left: 12px;
        color: rgba(204,204,204,1);
    }

    .emoji {
        position: absolute;
        bottom: 22px;
        left: 110px;
        width: 15px;
    }

    .recharge-icon {
        position: absolute;
        bottom: 23px;
        left: 168px;
        width: 20px;
    }

    .recharge-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 7px;
        color: rgba(255,255,255,1);
        position: absolute;
        bottom: 8px;
        left: 162px;
    }

    .request-icon {
        position: absolute;
        bottom: 23px;
        left: 205px;
        width: 20px;
    }

    .request-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 7px;
        color: rgba(255,255,255,1);
        position: absolute;
        bottom: 8px;
        left: 201px;
    }

    .album-icon {
        position: absolute;
        bottom: 23px;
        left: 239px;
        width: 20px;
    }

    .song-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 7px;
        color: rgba(255,255,255,1);
        position: absolute;
        bottom: 8px;
        left: 240px;
    }

    .share-icon {
        position: absolute;
        bottom: 25px;
        left: 272px;
        width: 17px;
    }

    .share-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 7px;
        color: rgba(255,255,255,1);
        position: absolute;
        bottom: 8px;
        left: 270px;
    }

    .back-button {
        position: absolute;
        top: 35px;
        left: 270px;
        cursor: pointer;
    }

    .album-cover-lyrics {
        position: absolute;
        top: 55px;
        left: 30px;
        width: 50px;
    }

    .now-playing {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 12px;
        color: rgba(255,255,255,1);
        position: absolute;
        top: 53px;
        left: 90px;
    }

    .song-name {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 12px;
        color: rgba(255,255,255,1);
        position: absolute;
        top: 53px;
        left: 167px;
    }

    .album-name {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 12px;
        color: rgba(255,255,255,1);
        position: absolute;
        top: 68px;
        left: 90px;
    }

    .song-lyrics {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 13px;
        color: rgba(48,27,48,1);
        position: absolute;
        top: 100px;
        height: 455px;
        overflow-y: auto;
        scrollbar-width: none;
    }

    .song-length {
        position: absolute;
        bottom: 15px;
    }
</style>