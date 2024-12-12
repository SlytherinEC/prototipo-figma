<script>
    // Puedes añadir lógica o props si es necesario

    import Boton from "./Boton.svelte";
import Logo from "./Logo.svelte";

  </script>
  
  <style>
    header {
      height: 16vh;
      width: 100vw;
      background-color: #FF8A66; 
      display: flex;
      align-items: center;
      justify-content: space-between;
      text-align: center;
      box-shadow: 0px 4px 6px rgba(255, 138, 102, 0.5); /* Sombra */
      padding: 0 20px;    
    }
    .contenedor-logo {
      height: 100%;
      display: flex;
      align-items: center;
    }
    .contenedor-botones {
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
  </style>
  
  <header>
    <div class="contenedor-logo">
      <Logo />
    </div>
    <div class="contenedor-botones">
      <Boton texto="SIGN IN" />
      <Boton texto="LOGIN" />
    </div>
  </header>
  