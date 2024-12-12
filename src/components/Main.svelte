<script>
    import NavBar from "./NavBar.svelte";
    import comics from "../data/comics.json"; // Importamos los datos del archivo JSON
    import FichaComic from "./FichaComic.svelte";
  
    // Opciones de la barra de navegación
    let navOptions = [
      "Inicio",
      "Comics",
      "Manga",
      "Novedades",
      "Especiales",
      "Salir",
    ];
  
    // Icono del carrito de compras
    import { FontAwesomeIcon } from "@fortawesome/svelte-fontawesome";
    import { faShoppingCart } from "@fortawesome/free-solid-svg-icons";
  </script>
  
  <main>
    <NavBar options={navOptions} />
    <div class="content">
      <div class="contenedor-opciones">
        <input type="text" name="buscar" placeholder="Buscar cómics..." />
        <div class="icono-carrito">
          <FontAwesomeIcon icon={faShoppingCart} />
        </div>
      </div>
      {#each comics as comic}
        <FichaComic {comic} />
      {/each}
    </div>
  </main>
  
  <style>
    main {
      flex-grow: 1; /* Ocupa el espacio restante en App */
      width: 100vw;
      height: 74vh;
      display: flex; /* Layout en fila */
    }
  
    .content {
      width: 84%;
      flex-grow: 1; /* Ocupa el resto del espacio no usado por NavBar */
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: #ffccb3; /* Color claro para el área de contenido */
      flex-wrap: wrap;
      overflow-y: auto; /* Permite el desplazamiento vertical */
      padding: 20px; /* Espaciado interno */
      box-sizing: border-box;
      height: 100%; /* Asegura que el contenedor ocupe todo el alto disponible */
    }
  
    /* Estilos para la barra de desplazamiento */
    .content::-webkit-scrollbar {
      width: 8px; /* Ancho de la barra de desplazamiento */
    }
  
    .content::-webkit-scrollbar-track {
      background: #ffccb3; /* Color de fondo de la pista */
      border-radius: 10px; /* Bordes redondeados en la pista */
    }
  
    .content::-webkit-scrollbar-thumb {
      background: #e63946; /* Color de la barra de desplazamiento */
      border-radius: 10px; /* Bordes redondeados */
    }
  
    .content::-webkit-scrollbar-thumb:hover {
      background: #d62828; /* Color de la barra al hacer hover */
    }
  
    .contenedor-opciones {
      width: 90%;
      height: 15%;
      background-color: #FFA48C;
      display: flex;
      align-items: center;
      flex-direction: row;
      justify-content: space-between; /* Distribuye el contenido entre los extremos */
      padding: 0 25px;
      border-radius: 8px;
    }
  
    input {
      width: 75%;
      height: 50%;
      border: none;
      background-color: #fff;
      color: #4A1C12;
      font-size: 18px;
      padding: 0 20px;
      box-sizing: border-box;
      border-radius: 50px;
    }
  
    .icono-carrito {
      font-size: 2rem;
      color: #4A1C12;
      cursor: pointer;
      transition: transform 0.2s;
    }
  
    .icono-carrito:hover {
      transform: scale(1.2);
    }

    /* Media Query para dispositivos móviles */
  @media (max-width: 768px) {
    
    .content {
      display: block; /* Cambia el display a bloque para que los elementos se apilen */
    }

    .contenedor-opciones {
      width: 100%; /* Asegura que el contenedor de opciones ocupe todo el ancho */
      height: auto;
      padding: 10px 15px;
      flex-direction: column; /* Alinea los elementos verticalmente */
      justify-content: center;
      align-items: center;
    }

    input {
      width: 100%; /* El input ocupa todo el ancho */
      height: 45px; /* Ajusta la altura para hacerlo más proporcional */
      font-size: 16px;
      padding: 0 15px;
    }

    .icono-carrito {
      font-size: 1.8rem; /* Ajusta el tamaño del icono en móvil */
    }
  }
  </style>
  