<script>
  let fonts = ["Roboto", "Syne Tactile", "Syne Mono", "Open Sans", "Trispace", "Noto Sans JP", "Lato", "Montserrat", "Turret Road", "Source Sans Pro", "Roboto Condensed", "Oswald", "Grandstander", "Roboto Mono", "Poppins", "Raleway", "Noto Sans", "Grenze Gotisch", "PT Sans", "Roboto Slab", "Merriweather", "Ubuntu", "Playfair Display", "Nunito", "Staatliches", "Open Sans Condensed", "Lora", "PT Serif", "Work Sans", "Noto Serif", "Rubik", "Henny Penny", "Fira Sans", "Noto Sans KR", "Hind Siliguri", "Mukta", "Titillium Web", "Nunito Sans", "Quicksand", "Nanum Gothic"];
  let font;

  function chooseRandomFont() {
    font = fonts[Math.floor(Math.random() * fonts.length)];
  }

  chooseRandomFont();

  function changeFont() {
    chooseRandomFont();
  }
</script>

<link href="https://fonts.googleapis.com/css2?family={font}&display=swap" rel="stylesheet">

<style>
div.card {
  height: 400px;
  width: 250px;
  border: 1px solid black;
  border-radius: 3%;
  margin: 0 auto;
  font-size: 200%;
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

  <p>Almost before we knew it, we had left the ground.</p>

  <div class="button-row">
    <button class="no" on:click={changeFont}>  
      NO!
    </button>

    <button class="yes" on:click={changeFont}>  
      YES!
    </button>
  </div>
</div>

