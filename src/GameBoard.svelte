<script>
    import { createEventDispatcher } from "svelte";
    
    const dispatch = createEventDispatcher();

    function handleOnClick(index) {
        dispatch("cell-clicked", index)
    };
    export let state;
</script>

<table>
    {#each state as item,i}
    {@const rootVal = Math.sqrt(state.length)}
    {#if i%rootVal == 0}
        <tr>
    {/if}
        
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <td 
            value = {item.label}
            on:click="{() => handleOnClick(i)}"
            style="background: {item.bgcolor}">
        {item.label}
        </td>    
    {/each}
</table>

<style>
    table {
        margin: auto;
        border: 1px solid #2b2a2a;
    }

    td {
        text-align: center;
        vertical-align: middle;
        width: 150px;
        height: 150px;
        border: 1px solid #000000;
        font-size: xx-large;
    }
</style>