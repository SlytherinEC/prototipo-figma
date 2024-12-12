<script>
    import NavBar from './NavBar.svelte';
  
    // Opciones de la barra de navegación
    let navOptions = ["Inicio", "Perfil", "Configuración", "Salir"];
  </script>
  
  <style>
    main {
      flex-grow: 1; /* Ocupa el espacio restante en App */
      width: 100%;
      display: flex; /* Layout en fila */
      background-color: #FFFFFF; /* Fondo del contenido principal */
    }
  
    .content {
      flex-grow: 1; /* Ocupa el resto del espacio no usado por NavBar */
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: #F5F5F5; /* Color claro para el área de contenido */
    }
  </style>
  
  <main>
    <NavBar options={navOptions} />
    <div class="content">
      <p>Contenido Principal</p>
    </div>
  </main>
  