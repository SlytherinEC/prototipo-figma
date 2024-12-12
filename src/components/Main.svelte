<script>
    import NavBar from "./NavBar.svelte";
    let navOptions = ["Inicio", "Perfil", "Configuración", "Salir"];

</script>

<main>
    <NavBar options={navOptions} />
    <div class="content">
        <p>Contenido Principal</p>
    </div>
</main>

<style>
    main {
        flex-grow: 1; /* Ocupa el espacio restante */
        width: 100%;
        background-color: #ffccb3; /* Cambia a tu color preferido */
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>
