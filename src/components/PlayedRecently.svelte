<script>
    import PlayedRecentlyBox from './PlayedRecentlyBox.svelte';

    export let playlist, cooldowns;
    let n = cooldowns.length;  
    let updateCooldown = 60_000;

    // // Update Cooldowns
    // function updateQueue(){  
    //     let i;
    //     for (i = 0; i < n; i++){
    //         cooldowns[i][3] = cooldowns[i][3] - 1;
    //         if (cooldowns[i][3] < 1){
    //            playlist.push(cooldowns.shift());
    //            n = n - 1;
    //            i--;
    //            if (n <= 0){
    //                 break;
    //            }
    //         }
    //     }
    // }  
    // $: if(n > 0){
    //     setInterval(updateQueue, updateCooldown);
    // }
  </script>
  
<main>
    <!-- Played Recently Table -->
    <table>
        <tr>
            <th> 
                Recently Played 
                {#if n != 0}
                <div class="numSongs">({cooldowns.length > 5 ? 5 : cooldowns.length} of {cooldowns.length} songs)</div>
                {/if}
            </th>
        </tr>

        <!-- Songs -->
        {#each cooldowns as row (row[0])}
        <tr>
            <td>
            <PlayedRecentlyBox>
                <span slot="cover"><img src={row[2]}/></span>
                <span slot="song">{row[0]}</span>
                <span slot="album">{row[1]}</span>
                <span slot="cooldown">{row[3]} min.</span>
            </PlayedRecentlyBox>
            </td>
        </tr>
        {/each}

        {#if n <= 0}
            <section>
                No songs played in the last 15 min.
            </section>
        {/if}
    </table>
</main>
  
<style>
    section{
        text-align: center;
        display: flex;
        flex-flow: column;
        justify-content: center;

        font-size: 15px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;

		width: 352px;
        height: 78px;
		padding-left: 16px;
		padding-right: 16px;
        border-radius: 10px;
		margin-bottom: 12px;
        background: #50504d
	}

    span[slot="song"]{
        font-size: 15px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
    }

    span[slot="album"]{
        font-size: 10px;
        color: #BFBFBF;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
    }

    span[slot="cooldown"]{
        font-size: 12px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 600;
        font-style: normal;
        font-variation-settings: "slnt" 0;
    }
    
    th{
        font-size: 18px;
        color: #F6F3F7;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
        text-align: left;
        padding-bottom: 12px;
    }

    .numSongs{
        display:inline; 
        font-size: 15px; 
        color: #BFBFBF
    }

</style>