<script>
	import ColorSelection from "./ColorSelection.svelte";
	import GameBoard from "./GameBoard.svelte";
	import ControlButtons from "./ControlButtons.svelte";

	let selectedColor;
	let boardSize = 4;
	
	let state;
	resetState();

    function updateColorForCell(event) {
		if(selectedColor == null) {
			alert("select a colour first");
			return;
		}
		const index = event.detail;
		console.log("hehe ");
		console.log(selectedColor);
		console.log(index);

		state[index].bgcolor = selectedColor;
		state = state;
    }

	function resetState() {
		let totalBlocks = Math.pow(boardSize, 2);
		state = Array(totalBlocks).fill(0).map((_, index) => {
			return {
				label: index + 1,
				bgcolor: "#ffffff"
			}
		});
	}

	function shuffle() {
		state.sort(() => (Math.random() > .5) ? 1 : -1);
		state = state;
	}
</script>

<main>
	<ColorSelection bind:color={selectedColor} />
	<br>
	<br>
	<GameBoard 
		on:cell-clicked = {updateColorForCell}
		bind:state={state}
	/>
	<br>
	<br>
	<ControlButtons
		on:reset={resetState}
		on:shuffle={shuffle}
	/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: auto;
	}
</style>