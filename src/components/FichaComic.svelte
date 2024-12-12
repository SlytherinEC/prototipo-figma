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
      background-color: #fff;
      box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    }
  
    .portada {
      flex: 1;
      background-size: cover;
      background-position: center;
    }
  
    .info {
      padding: 10px;
      font-size: 14px;
      display: flex;
      flex-direction: column;
      gap: 5px;
    }
  
    .info h3 {
      margin: 0;
      font-size: 16px;
      font-weight: bold;
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
    <div
      class="portada"
      style="background-image: url('{comic.imagen}');"
    ></div>
    <div class="info">
      <h3>{comic.titulo}</h3>
      <p>Autor: {comic.autor}</p>
      <p>Editorial: {comic.editorial}</p>
      <p>Género: {comic.genero}</p>
      <p class="precio">Precio: ${comic.precio}</p>
      <p>Stock: {comic.stock}</p>
    </div>
  </div>
  