<script>
	import ColorSelection from "./ColorSelection.svelte";
	import GameBoard from "./GameBoard.svelte";
	import ControlButtons from "./ControlButtons.svelte";

	let selectedColor;
	
	let state;
	resetState();

    function updateColorForCell(index) {
		if(selectedColor == null) {
			alert("select a colour first");
			return;
		}
		console.log(selectedColor);
		console.log("hehe , " + index);

		state[index - 1].bgcolor = selectedColor;
		state = state;
    }

	function resetState() {
		state = Array(9).fill(0).map((_, index) => {
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
		bind:selectedColor={selectedColor}
		handleOnClick = {updateColorForCell}
		bind:state={state}
	/>
	<br>
	<br>
	<ControlButtons
		onReset={resetState}
		onShuffle={shuffle}
	/>
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