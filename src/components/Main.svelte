<script>
    import NavBar from "./NavBar.svelte";
    import comics from "../data/comics.json"; // Importamos los datos del archivo JSON
    // Opciones de la barra de navegación
    let navOptions = ["Inicio", "Perfil", "Configuración", "Salir"];
    import FichaComic from "./FichaComic.svelte";
</script>

<main>
    <NavBar options={navOptions} />
    <div class="content">
        {#each comics as comic}
            <FichaComic {comic} />
        {/each}
    </div>
</main>

<style>
    main {
        flex-grow: 1; /* Ocupa el espacio restante en App */
        width: 100vw;
        height: 77vh;
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
    }</style>
