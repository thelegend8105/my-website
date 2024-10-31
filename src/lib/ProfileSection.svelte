<section id="profile">
  <img src="/rht9bit.png" alt="Rohith" />
  <article>
    <h1>Rohith</h1>
    <p>
      {new Date().getFullYear() - 2005} year old developer from Bangalore, Karnataka.
    </p>
  </article>
</section>

<style>
  section#profile {
    width: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: start;
    gap: 2rem;

    img {
      width: 6rem;
      height: 6rem;
      border-radius: 9999px;
    }

    article {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;

      h1 {
        font-size: 1.5rem;
      }

      p {
        color: var(--color-text-secondary);
      }
    }
  }
</style>
