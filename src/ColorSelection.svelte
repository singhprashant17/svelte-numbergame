<script>
    export var color
</script>

<form>
    
    <input type="radio" bind:group={color} name="color" value={"#FF0000"}>RED
    <input type="radio" bind:group={color} name="color" value={"#00FF00"}>GREEN
    <input type="radio" bind:group={color} name="color" value={"#0000FF"}>BLUE

</form>


<style>
    input {
        margin-left: 20px;
        margin-right: 5px;
    }
</style>