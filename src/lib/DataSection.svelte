<script>
  /**
   * @typedef {Object} DataInput
   * @property {string} title
   * @property {string} [description]
   * @property {number} [year]
   * @property {string} [type]
   * @property {string} [link]
   */

  /** @type {{ title: string, data: Array<DataInput> }} */
  const { title, data } = $props();
</script>

<section id="data-section">
  <h2>{title}</h2>
  {#each data as item}
    <article>
      {#if item.type || item.year}
        <span id="type">
          {item.type || item.year}
        </span>
      {/if}
      <div class="contents">
        {#if item.link}
          <a href={item.link}>
            <h3>{item.title}</h3>
          </a>
        {:else}
          <h3>{item.title}</h3>
        {/if}
        {#if item.description}
          <p>{item.description}</p>
        {/if}
      </div>
    </article>
  {/each}
</section>

<style>
  section#data-section {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
    gap: 1rem;

    article {
      display: grid;
      grid-template-columns: 6rem 1fr;
      width: 100%;
      gap: 2rem;
      @media (max-width: 600px) {
        grid-template-columns: 1fr;
        gap: 0.15rem;
      }

      span#type {
        color: var(--color-text-secondary);
      }

      div.contents {
        display: flex;
        flex-direction: column;
        gap: 0.25rem;

        h3 {
          color: var(--color-text-primary);
        }

        p {
          color: var(--color-text-secondary);
        }
      }

      a {
        width: fit-content;
        text-decoration: none;

        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
</style>
