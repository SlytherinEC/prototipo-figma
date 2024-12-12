<script>
    // Lista de opciones de navegación
    export let options = ["Inicio", "Perfil", "Configuración", "Salir"];
  </script>
  
  <style>
    nav {
      width: 16%; /* 16% del ancho de Main */
      height: 100%; /* Todo el alto de Main */
      background-color: #FFA48C; /* Fondo */
      color: #4A1C12; /* Texto oscuro que resalte */
      display: flex;
      flex-direction: column;
      align-items: flex-start; /* Alinear elementos al inicio */
      justify-content: center; /* Centrar verticalmente */
      padding: 20px;
      box-sizing: border-box;
    }
  
    a {
      text-decoration: none; /* Sin subrayado */
      color: inherit; /* Usa el color del texto definido en nav */
      font-size: 18px;
      margin-bottom: 10px;
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
  