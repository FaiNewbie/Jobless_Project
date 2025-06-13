<script>
  import Tube from "/src/assets/Tube.svg";

  let { nameButton } = $props();
  function handleClick() {
    alert("You clicked the button!");
  }
</script>

<!-- svelte-ignore event_directive_deprecated -->
<button on:click={handleClick}>
  <img src={Tube} class="logo svelte" alt="Tube Logo" />
  <span class="name button">{nameButton}</span>
</button>

<style>
  .logo {
    height: 1.2em;
    opacity: 0;
    transition:
      opacity 500ms ease-in,
      transform 0.3s ease-in;
  }

  button {
    background: none;
    border: none;
    font-size: 2em;
    font-family: "Kanit", sans-serif;
    font-weight: 200;
    text-decoration: none;
    letter-spacing: 10px;
    margin: 2rem;
    cursor: pointer;
    color: rgba(255, 255, 255, 0.3);
    transition: color 0.3s ease-in;
  }

  button:hover,
  button:hover .logo {
    color: rgb(255, 255, 255, 0.8);
    text-shadow: 0px 0px 10px #ffffff;
    filter: drop-shadow(0 0 20px #ffffff);
    opacity: 1;
  }

  button:hover .logo {
    transform: rotate(45deg);
  }

  button:hover .name {
    text-decoration: underline;
  }
</style>
