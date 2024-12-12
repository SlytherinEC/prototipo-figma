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
        overflow-y: scroll; /* Permite el desplazamiento vertical */
        padding: 20px; /* Espaciado interno */
        box-sizing: border-box;
    }
</style>
