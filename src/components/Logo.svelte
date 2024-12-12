<script>
    // Importar la imagen desde la carpeta src/img
    import logo from "../img/logo.jpg";
  </script>
  
  <style>
    .logo-container {
      height: 70%;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }

    .logo-container > img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      object-position: center;
      object-fit: cover;
      border-radius: 50%; /* Hace que el div tenga forma circular */
    }
  </style>
  
  <div class="logo-container">
    <img src="{logo}" alt="Logo de la aplicación" />
  </div>
  