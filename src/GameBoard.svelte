<script>
    export let handleOnClick = (cellId) => {};
    export let selectedColor;
</script>

<table>
    <tr>
        <td id="1" value="1" on:click={handleOnClick(1)}>1</td>
        <td id="2" value="2" on:click={handleOnClick(2)}>2</td>
        <td id="3" value="3" on:click={handleOnClick(3)}>3</td>
    </tr>
    
    <tr>
        <td id="4" value="4" on:click={handleOnClick(4)}>4</td>
        <td id="5" value="5" on:click={handleOnClick(5)}>5</td>
        <td id="6" value="6" on:click={handleOnClick(6)}>6</td>
    </tr>
    
    <tr>
        <td id="7" value="7" on:click={handleOnClick(7)}>7</td>
        <td id="8" value="8" on:click={handleOnClick(8)}>8</td>
        <td id="9" value="9" on:click={handleOnClick(9)}>9</td>
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
        width: 400px;
        height: 400px;
        margin-left: auto;
        margin-right: auto;
        border: 1px solid #2b2a2a;
        font-size: xx-large;
    }

    td {
        border: 1px solid #000000;
    }
</style>