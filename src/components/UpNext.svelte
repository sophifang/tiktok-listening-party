<script>
    import UpNextBox from './UpNextBox.svelte';
    import { flip } from 'svelte/animate';

    export let playlist;
    let pos = {};
    let updateCooldown = 500;
    let greenArrow = "green-arrow.png";
    let redArrow = "red-arrow.png";
    $: n = playlist.length;  

    function sortPlaylist()  
    {  
        let i, j, song;

        pos[playlist[0][0]] = 0;
        for (i = 1; i < n; i++){  
            song = playlist[i];  
            j = i - 1;
            pos[playlist[i][0]] = i;

            while (j >= 0 && playlist[j][3] < song[3]){  
                playlist[j + 1] = playlist[j];  
                j = j - 1;  
            }  
            playlist[j + 1] = song;
        }  
    }  
    $: setInterval(sortPlaylist, updateCooldown);
  </script>
  
<main>
    <!-- Up Next Table -->
    <table>
        <tr>
            <th>Up Next <div class="numSongs">({playlist.length > 5 ? 5 : playlist.length} of {n} songs)</div></th>
        </tr>

        <!-- Songs -->
        {#each playlist.slice(0, 5) as row, currPos (row[0])}
        <tr animate:flip={{duration:500}}>
            <td>
            <UpNextBox>
                <span slot="cover"><img src={row[2]} width="42px" height="42px"/></span>
                <span slot="song">{row[0]}</span>
                <span slot="album">{row[1]}</span>
                <span slot="boost">
                    {#if pos[row[0]] > currPos}
                        <div id="image" class='centerBoost'>
                            <img src={greenArrow} width="14px" height="17px"/>
                        </div>
                    {:else if pos[row[0]] < currPos}
                        <div id="image">
                            <img src={redArrow} width="14px" height="17px"/>
                        </div>
                    {:else}
                        {row[3]}
                        <br/>
                        {#if row[3] > 1}
                            boosts
                        {:else}
                            boost
                        {/if}
                    {/if}
                </span>
            </UpNextBox>
            </td>
        </tr>
        {/each}
    </table>
</main>
  
<style>
    span[slot="song"]{
        font-size: 10px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
    }

    span[slot="album"]{
        font-size: 7px;
        color: #BFBFBF;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
    }

    span[slot="boost"]{
        font-size: 8px;
        color: #D9D9D9;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
    }

    span[slot="cover"]{
        width: 42px;
        height: 42px;
    }

    
    th{
        font-size: 12px;
        color: #F6F3F7;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        font-variation-settings: "slnt" 0;
        text-align: left;
        padding-bottom: 6px;
    }

    .centerBoost{
        color:#4EB77B;
        font-size: 15px;
        font-family: "Inter", sans-serif;
        font-optical-sizing: auto;
        font-weight: 500;
        font-style: normal;
        font-variation-settings: "slnt" 0;
        height: 100%;
        width: 100%;
        display: flex;
        justify-content: right;
        align-items: center;
        white-space: pre;
    }

    .numSongs{
        display:inline; 
        font-size: 10px; 
        color: #BFBFBF
    }
</style>