<script>
    export let comic; // Objeto del cómic recibido como prop
</script>

<style>
  .ficha-comic {
    display: flex;
    flex-direction: column;
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    background-color: #FF8A66;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    width: 18%; /* Ancho fijo: 18% del contenedor */
    height: 35%; /* Alto fijo: 35% del contenedor */
    box-sizing: border-box;
    margin: 2%;
  }

  .portada {
    height: 50%; /* Ocupa el 50% del contenedor */
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #FF5733; /* Fondo claro para resaltar la imagen */
  }

  .portada img {
    max-width: 100%; /* Se adapta al ancho del contenedor */
    max-height: 100%; /* Se adapta al alto del contenedor */
    object-fit: contain; /* Ajusta la imagen sin recortarla */
  }

  .info {
    height: 50%; /* Ocupa el 50% del contenedor */
    padding: 10px;
    font-size: 14px;
    display: flex;
    flex-direction: column;
    gap: 5px;
    box-sizing: border-box;
  }

  .info h3 {
    margin: 0;
    font-size: 16px;
    font-weight: bold;
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden; /* Evita que el texto se desborde */
  }

  .info p {
    margin: 0;
    font-size: 13px;
    color: #555;
  }

  .precio {
    font-size: 14px;
    font-weight: bold;
    color: #e63946;
  }
</style>

<div class="ficha-comic">
  <div class="portada">
    <img src="{comic.imagen}" alt="{comic.titulo}" />
  </div>
  <div class="info">
    <h3>{comic.titulo}</h3>
    <p>Autor: {comic.autor}</p>
    <p>Editorial: {comic.editorial}</p>
    <p>Género: {comic.genero}</p>
    <p class="precio">Precio: ${comic.precio}</p>
    <p>Stock: {comic.stock}</p>
  </div>
</div>
