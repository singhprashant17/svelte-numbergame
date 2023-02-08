<script>
    export let onReset = () => {};
    export let onShuffle = () => {};
</script>

<input id="but" type="button" value="Reset" on:click={onReset}>
<input id="shuf" type="button" value="Shuffle" on:click={onShuffle}>
