<script>
    export var boardSize;
</script>

<label for="languages">Select Board Size</label>

<select name="board-size" id="board-size" bind:value="{boardSize}">
    {#each Array(10) as _, i}
        {@const newValue = i + 1}
        {#if newValue > 1}
            <option value={newValue}>{newValue} X {newValue}</option>
        {/if}
    {/each}
</select>
