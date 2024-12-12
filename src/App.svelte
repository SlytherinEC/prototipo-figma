<script>
  import Header from './components/Header.svelte';
  import Main from './components/Main.svelte';
  import Footer from './components/Footer.svelte';
</script>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .container {
    display: flex;
    flex-direction: column;
    height: 100vh; /* Ocupa toda la altura de la ventana */
    width: 100vw; /* Ocupa todo el ancho de la ventana */
    font-family: sans-serif;
    font-size: 18px;
    font-weight: bold;
  }
</style>

<div class="container">
  <Header />
  <Main />
  <Footer />
</div>
