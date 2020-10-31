<script>
  import fonts from "./fontlist.js";
  let font;

  function chooseRandomFont() {
    font = fonts[Math.floor(Math.random() * fonts.length)];
  }

  chooseRandomFont();

  function swipeNo() {
    console.log("You swiped no:", font)
    chooseRandomFont();
  }

  function swipeYes() {
    console.log("You swiped yes:", font)
    chooseRandomFont();
  }
</script>

<link href="https://fonts.googleapis.com/css2?family={font}&display=swap" rel="stylesheet">

<style>
div.card {
  height: 600px;
  width: 350px;
  border: 1px solid black;
  border-radius: 3%;
  margin: 0 auto;
  font-size: 250%;
  font-family: var(--card-font);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}

button {
    height: 50px;
    width: 100px;
    border: none;
    margin: 0 auto;
}

p {
  padding: 5px;
}

h6 {
  padding: 0;
  margin: 0;
}

.button-row {
  margin-bottom: 10px;
}

.yes {
    background-color: #8db596;
}

.no {
    background-color: #ee6f57;
}

</style>

<div class="card" style="--card-font: '{font}'">
  <h6>{font}</h6>
  <p>Almost before we knew it, we had left the ground.</p>

  <div class="button-row">
    <button class="no" on:click={swipeNo}>
      NO!
    </button>

    <button class="yes" on:click={swipeYes}>
      YES!
    </button>
  </div>
</div>
