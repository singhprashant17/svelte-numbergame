<script>
    export let handleOnClick = (index) => {};
    export let state;
</script>

<table>
    <tr>
        <td id="1" value={state[0].label} on:click={handleOnClick(1)} style="background: {state[0].bgcolor}">{state[0].label}</td>
        <td id="2" value={state[1].label} on:click={handleOnClick(2)} style="background: {state[1].bgcolor}">{state[1].label}</td>
        <td id="3" value={state[2].label} on:click={handleOnClick(3)} style="background: {state[2].bgcolor}">{state[2].label}</td>
    </tr>
    
    <tr>
        <td id="4" value={state[3].label} on:click={handleOnClick(4)} style="background: {state[3].bgcolor}">{state[3].label}</td>
        <td id="5" value={state[4].label} on:click={handleOnClick(5)} style="background: {state[4].bgcolor}">{state[4].label}</td>
        <td id="6" value={state[5].label} on:click={handleOnClick(6)} style="background: {state[5].bgcolor}">{state[5].label}</td>
    </tr>
    
    <tr>
        <td id="7" value={state[6].label} on:click={handleOnClick(7)} style="background: {state[6].bgcolor}">{state[6].label}</td>
        <td id="8" value={state[7].label} on:click={handleOnClick(8)} style="background: {state[7].bgcolor}">{state[7].label}</td>
        <td id="9" value={state[8].label} on:click={handleOnClick(9)} style="background: {state[8].bgcolor}">{state[8].label}</td>
    </tr>
</table>

<!-- <table>
    {#each Array(3) as _, i}
        <tr>
            {#each Array(3) as _, j}
                <td value="j">{count}</td>
                {count = count+1}
            {/each}
        </tr>
    {/each}
</table> -->

<style>
    table {
        margin-left: auto;
        margin-right: auto;
        border: 1px solid #2b2a2a;
        font-size: xx-large;
    }

    td {
        width: 150px;
        height: 150px;
        border: 1px solid #000000;
        flex: 1;
    }
</style>