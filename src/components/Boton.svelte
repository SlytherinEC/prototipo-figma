<script>
    export let texto; // El texto que se mostrará en el botón
  </script>
  
  <style>
    .boton {
      width: 8%; /* Ancho del botón */
      height: 24%; /* Alto del botón */
      background-color: #FF5733; /* Color de fondo */
      color: #FFD700; /* Color del texto */
      font-size: 16px;
      font-weight: bold;
      text-align: center;
      line-height: 1.5;
      border: 10px solid transparent; /* Borde transparente para mantener el estilo de bordes redondeados */
      border-radius: 8px;
      box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.2); /* Sombra abajo y a la derecha */
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); /* Sombreado del texto */
      cursor: pointer;
      transition: background-color 0.3s ease, box-shadow 0.3s ease;
    }
  
    .boton:hover {
      background-color: #e04e26; /* Color de fondo al pasar el mouse */
      box-shadow: 7px 7px 15px rgba(0, 0, 0, 0.3); /* Sombra al hacer hover */
    }
  </style>
  
  <button class="boton">
    {texto}
  </button>
  