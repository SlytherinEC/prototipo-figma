<script>
  import { FontAwesomeIcon } from "@fortawesome/svelte-fontawesome";
  import { faFacebook, faTwitter, faInstagram, faGithub } from "@fortawesome/free-brands-svg-icons";
  import { faEnvelope } from "@fortawesome/free-solid-svg-icons";

  const currentYear = new Date().getFullYear(); // Obtiene el año actual
</script>

<footer>
    <div class="project-info">
    <p>Tienda de cómics &copy; {currentYear}. Todos los derechos reservados.</p>
  </div>
<div class="social-icons">
    <a href="https://github.com/SlytherinEC/prototipo-figma.git" target="_blank" class="icon">
      <FontAwesomeIcon icon={faGithub} />
    </a>
    <a href="mailto:yborges2005@gmail.com" class="icon">
      <FontAwesomeIcon icon={faEnvelope} />
    </a>
  </div>
</footer>

<style>
  footer {
    height: auto;
    width: 100vw;
    background-color: #FF8A66;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    padding: 10px;
    color: #fff;
    text-align: center;
  }

  .social-icons {
    display: flex;
    gap: 10px;
    margin-bottom: 10px; /* Separación del texto */
  }

  .icon {
    color: #fff;
    font-size: 1.5rem;
    cursor: pointer;
    transition: transform 0.2s;
  }

  .icon:hover {
    transform: scale(1.2);
  }

  .project-info {
    font-size: 0.9rem;
  }
</style>
