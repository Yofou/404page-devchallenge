<script>
  import scarescrow from './assets/Scarecrow.png'
  import Button from './lib/Button.svelte'
</script>

<main>
  <h1>404 not found</h1>

  <img class="scarecrow" src={scarescrow} alt="scarecrow">

  <section>
    <h1>I have bad news for you</h1>
    <p>The page you are looking for might be removed or is temporarily unavailable</p>
    <Button --margin="28px 0">back to homepage</Button>
  </section>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@700&family=Space+Mono:wght@400;700&display=swap');

  :root {
    --dark-grey: #333333;
    --light-grey: #4F4F4F;
  }

  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  main {
    width: 100vw;
    height: 100vh;

    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    font-family: 'Space Mono', monospace;
  }

  main > h1 {
    position: absolute;
    top: 40px;
    left: 70px;

    font-family: 'Inconsolata', monospace;
    font-size: 24px;
    font-weight: 700;
  }

  section {
    display: grid;
    grid-auto-flow: row;

    height: min-content;
    place-self: center;
    gap: 36px;
  }

  section h1 {
    width: clamp(0ch, 95%, 20ch);
    color: var(--dark-grey);

    font-size: 64px;
    font-weight: 700;
    letter-spacing: 0.035em;

    align-self: end;
  }

  section p {
    width: 26ch;
    color: var(--light-grey);

    font-size: 24px;
    letter-spacing: -0.035em;
    line-height: 36px;

    align-self: center;
  }

  .scarecrow {
    width: 539.22px;
    height: 447.43px;

    place-self: center;
  }

  @media (max-width: 922px) {
    main {
      grid-template-rows: 1fr 1fr;
      grid-template-columns: 1fr;
      padding-left: 23px;
    }

    main > h1 {
      top: 20px;
      left: 24px;      
    }

    .scarecrow {
      width: 286.83px;
      height: 238px;
      transform: translateX(-23px);
    }

    section {
      gap: 30px;
      transform: translateY(-65px);
    }

    section h1 {
      font-size: 48px;
      letter-spacing: -0.035em;
    }

    section p {
      font-size: 18px;
    }
  }
</style>
