<script>
    // Lista de opciones de navegación
    export let options = [];
  </script>
  
  <style>
    nav {
      width: 16%; /* 16% del ancho de Main */
      height: 100%; /* Todo el alto de Main */
      background-color: #FFA48C; /* Fondo */
      color: beige; /* Texto oscuro que resalte */
      text-shadow: 2px 2px 4px #4A1C12; /* Sombreado del texto */
      display: flex;
      flex-direction: column;
      align-items: flex-start; /* Alinear elementos al inicio horizontal */
      justify-content: flex-start; /* Alinear elementos al inicio vertical */
      padding: 20px;
      box-sizing: border-box;
      box-shadow: 4px 0px 6px rgba(255, 164, 140, 0.5); /* Sombra hacia la derecha */
    }
  
    a {
      text-decoration: none; /* Sin subrayado */
      color: inherit; /* Usa el color del texto definido en nav */
      font-size: 18px;
      margin-bottom: 10px; /* Espaciado entre los enlaces */
      transition: color 0.3s;
    }
  
    a:hover {
      color: #7A2E1F; /* Color más oscuro al pasar el cursor */
    }
  </style>
  
  <nav>
    {#each options as option}
      <a href="#">{option}</a>
    {/each}
  </nav>
  