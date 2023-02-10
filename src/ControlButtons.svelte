<script>
    import {createEventDispatcher} from "svelte";

    const dispatch = createEventDispatcher();

    function onReset() {
        dispatch("reset");
    };
    function onShuffle() {
        dispatch("shuffle");
    };
</script>

<input id="but" type="button" value="Reset" on:click={onReset}>
<input id="shuf" type="button" value="Shuffle" on:click={onShuffle}>
