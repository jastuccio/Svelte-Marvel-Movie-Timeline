<script>
  import MarvelMovies from "./MarvelMovies.js";

  let index = 0;

  function nextMovie() {
    index = (index + 1) % MarvelMovies.length;
  }

  function prevMovie() {
    index = index - 1;
    if (index < 0) {
      index = MarvelMovies.length - 1;
    }
  }
</script>

<style>
  h1 {
  }
</style>

<h1>Marvel Move Timeline</h1>

<button on:click={prevMovie}>👈</button>

<p>Current movie: {MarvelMovies[index].title}</p>

<button on:click={nextMovie}>👉</button>

<p>
  Borrowed from
  <a
    href="https://www.amctheatres.com/amc-scene/the-best-way-to-rewatch-the-mcu">
    AMC Movies | Watch The Marvel Movies In Order
  </a>
</p>
