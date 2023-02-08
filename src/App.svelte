<script>
	import ColorSelection from "./ColorSelection.svelte";
	import GameBoard from "./GameBoard.svelte";
	import ControlButtons from "./ControlButtons.svelte";

	let selectedColor

    function updateColorForCell(cellId) {
		if(selectedColor == null) {
			alert("select a colour first");
			return false;
		}
		console.log(selectedColor);
		console.log("hehe , " + cellId);

        document.getElementById(cellId).style.backgroundColor = selectedColor;
    }
</script>

<main>
	<ColorSelection bind:color={selectedColor} />
	<br>
	<br>
	<GameBoard 
		bind:selectedColor={selectedColor}
		handleOnClick = {updateColorForCell}
	/>
	<br>
	<br>
	<ControlButtons/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>