<script>
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
            <div class="box">
                <p class="title">So Long, London</p>
                <img src="album.png" alt="Album cover" class="album-cover-home">
                <div class="click-lyrics" on:click={next}>
                    <span> Stopped trying to drill the safe <br> </span>
                    <span class="different-color"> Thinkin, how much sad did <br> </span>
                    <span class="different-color"> you think I had <br> </span>
                    <span> Did you think I had in me? </span>
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
        <div class = "second">
            <div class="box">
                <img src="album.png" alt="Album cover" class="album-cover-lyrics">
                <div class="back-button" on:click={back}>
                    <img src="left_arrow.png" width="20"/>
                </div>
                <p class="now-playing">Now Playing: </p>
                <p class="song-name"> So Long, London </p> <br>
                <p class="album-name"> The Tortured Poets Department </p>
                <p class="song-lyrics">
                    <span> I saw in my mind fairy lights <br> </span>
                    <span> through the mist <br> </span>
                    <span> I kept calm and carried the <br> </span>
                    <span> weight of the rift <br> </span>
                    <span> Pulled him in tighter each time <br> </span>
                    <span> he was drifting away <br> </span>
                    <span> My spine split from carrying <br> </span>
                    <span> us up the hill <br> </span>
                    <span> Wet through my clothes, <br> </span>
                    <span> weary bones caught the chill <br> </span>
                    <span> I stopped trying to make him laugh <br> </span>
                    <span> Stopped trying to drill the safe <br> </span>
                    <span class="different-color"> Thinkin, how much sad did <br> </span>
                    <span class="different-color"> you think I had <br> </span>
                    <span> Did you think I had in me? <br> </span>
                    <span> Oh, the tragedy ... <br> </span>
                    <span> So long, London <br> </span>
                    <span> You'll find someone ... <br> </span>
                    <span> I didn't opt in to be your odd man out <br> </span>
                    <span> I founded the club she's heard <br> </span>
                    <span> great things about <br> </span>
                    <span> I left all I knew, you left me at <br> </span>
                    <span> the house by the Heath <br> </span>
                    <span> I stopped CPR, after all it's no use <br> </span>
                    <span> The spirit was gone, <br>  </span>
                    <span> we would never come to <br> </span>
                    <span> And I'm pissed off you let me give <br> </span>
                    <span> you all that youth for free <br> </span>
                    <span> For so long, London <br> </span>
                    <span> Stitches undone <br> </span>
                    <span> Two graves, one gun <br> </span>
                    <span> I'll find someone ... <br> </span>
                    <span> And you say I abandoned the ship <br> </span>
                    <span> But I was going down with it <br> </span>
                    <span> My white knuckle dying grip <br> </span>
                    <span> Holding tight to your quiet <br> </span>
                    <span> resentment and <br> </span>
                    <span> My friends said it isn't right <br> </span>
                    <span> to be scared <br> </span>
                    <span> Every day of a love affair <br> </span>
                    <span> Every breath feels like rarest air <br> </span>
                    <span> When you're not sure if he <br> </span>
                    <span> wants to be there <br> </span>
                    <span> So how much sad did you think I had, <br> </span>
                    <span> Did you think I had in me? <br> </span>
                    <span> How much tragedy? <br> </span>
                    <span> Just how low did you think I'd go? <br> </span>
                    <span> Before I'd self-implode <br> </span>
                    <span> Before I'd have to go be free <br> </span>
                    <span> You swore that you loved me but <br> </span>
                    <span> where were the clues? <br> </span>
                    <span> I died on the altar waiting for the proof <br> </span>
                    <span> You sacrificed us to the gods of <br> </span>
                    <span> your bluest days <br> </span>
                    <span> And I'm just getting color back <br> </span>
                    <span> into my face <br> </span>
                    <span> I'm just mad as hell cause I <br> </span>
                    <span> loved this place <br> </span>
                    <span> For so long, London <br> </span>
                    <span> Had a good run <br> </span>
                    <span> A moment of warm sun <br> </span>
                    <span> But I'm not the one <br> </span>
                    <span> So long, London <br> </span>
                    <span> Stitches undone <br> </span>
                    <span> Two graves, one gun <br> </span>
                    <span> You'll find someone ... <br> </span>
                </p>
                <img src="song_length.png" alt="Song length" class="song-length">
            </div>
        </div>
    {/if}
</main>

<style>
    .box {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        width: 330px;
        height: 632px;
        background: rgb(178,177,173);
        background: linear-gradient(-184deg, rgba(178,177,173,1) 0%, rgba(133,132,129,1) 21%);
        border-radius: 12px;
    }

    .title {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 16px;
        color: white;
        position: absolute;
        top: 130px;
        left: 97px;
    }

    .album-cover-home {
        position: absolute;
        top: 180px;
        left: 70px;
        width: 180px;
        height: auto;
    }

    .click-lyrics {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 13px;
        color: #424242;
        position: absolute;
        bottom: 195px;
        cursor: pointer;
    }

    .different-color {
        color: white;
    }

    .comment-box {
        font-family: 'Inter', sans-serif;
        font-size: 14px;
        position: absolute;
        bottom: 20px;
        left: 20px;
        width: 140px;
        padding: 8px;
        border: none;
        border-radius: 15px;
        background-color: rgba(247,245,245,1);
        box-sizing: border-box;
    }

    .emoji {
        position: absolute;
        bottom: 27px;
        left: 135px;
        width: 20px;
        height: auto;
    }

    .recharge-icon {
        position: absolute;
        bottom: 27px;
        left: 175px;
        width: 30px;
        height: auto;
    }

    .recharge-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 8px;
        color: white;
        position: absolute;
        bottom: 14px;
        left: 172px;
    }

    .request-icon {
        position: absolute;
        bottom: 27px;
        left: 215px;
        width: 30px;
        height: auto;
    }

    .request-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 8px;
        color: white;
        position: absolute;
        bottom: 14px;
        left: 215px;
    }

    .album-icon {
        position: absolute;
        bottom: 27px;
        left: 255px;
        width: 30px;
        height: auto;
    }

    .song-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 8px;
        color: white;
        position: absolute;
        bottom: 14px;
        left: 260px;
    }

    .share-icon {
        position: absolute;
        bottom: 25px;
        left: 290px;
        width: 30px;
        height: auto;
    }

    .share-text {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 8px;
        color: white;
        position: absolute;
        bottom: 14px;
        left: 293px;
    }

    .back-button {
        position: absolute;
        top: 40px;
        left: 290px;
        height: auto;
        cursor: pointer;
    }

    .album-cover-lyrics {
        position: absolute;
        top: 70px;
        left: 30px;
        width: 60px;
        height: auto;
    }

    .now-playing {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 13px;
        color: white;
        position: absolute;
        top: 70px;
        left: 100px;
    }

    .song-name {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 13px;
        color: white;
        position: absolute;
        top: 70px;
        left: 180px;
    }

    .album-name {
        font-family: 'Inter', sans-serif;
        font-weight: normal;
        font-size: 13px;
        color: white;
        position: absolute;
        top: 90px;
        left: 100px;
    }

    .song-lyrics {
        font-family: 'Inter', sans-serif;
        font-weight: bold;
        font-size: 13px;
        color: #424242;
        position: absolute;
        top: 130px;
        height: 440px;
        overflow-y: auto;
        scrollbar-width: none;
    }

    .song-length {
        position: absolute;
        bottom: 20px;
        left: 30px;
        width: 270px;
        height: auto;
    }
</style>