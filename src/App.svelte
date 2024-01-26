<script>
  // @ts-ignore
  import Nested from "/src/Nested.svelte";
  let name = "svelte";
  let number1 = 4;
  let number2 = 6;
  let src = "./src/assets/alien.png";
  let kokot = "<p><b>Kokot</b></p>";
  let count = 0;
  $: doubled = count * 2;
	function increment() {
		count += 1;
	}
</script>

<html lang="en">
  <body>
    <h1>Hello {name.toUpperCase()}!</h1>
    <p>{number1} + {number2} = {number1 + number2}</p>
    <img {src} alt="hajzl" />
    <Nested />
    {@html kokot}
    <button on:click={increment}>
      Clicked {count}
      {count === 1 ? "time" : "times"}
    </button>
  </body>
</html>

<style>
  body {
    display: flex;
    flex-direction: column;
  }
  p {
    color: goldenrod;
    font-family: "Courier New", Courier, monospace;
    font-size: 2em;
  }
</style>
