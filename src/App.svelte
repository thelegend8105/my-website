<script>
  import ProfileSection from "./lib/ProfileSection.svelte";
  import DataSection from "./lib/DataSection.svelte";

  const data = [
    {
      title: "Projects",
      data: [
        {
          title: "Rohith.codes",
          description: "My personal website",
          link: "https://rohith.codes",
          year: 2024,
        },
        {
          title: "Hexage Wiki",
          description: "A wiki for Hexage games",
          link: "https://hexage.wiki",
          year: 2024,
        },
      ],
    },
    {
      title: "Education",
      data: [
        {
          title: "University",
          description: "Manipal Institute of Technology - Bangalore",
          year: 2024,
        },
        {
          title: "College",
          description: "Presidency Composite PU College",
          year: 2022,
        },
        {
          title: "High School",
          description: "Presidency School",
          year: 2012,
        },
      ],
    },
    {
      title: "Contacts",
      data: [
        {
          title: "thelegend8105@gmail.com",
          link: "mailto:thelegend8105@gmail.com",
          type: "Email",
        },
        {
          title: "thelegend8105",
          link: "https://github.com/thelegend8105",
          type: "Github",
        },
      ],
    },
  ];
</script>

<main>
  <ProfileSection />
  {#each data as item}
    <DataSection title={item.title} data={item.data} />
  {/each}
</main>

<style>
  main {
    margin-left: auto;
    margin-right: auto;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
    height: 100vh;
    max-width: 768px;
    width: 100%;
    overflow-x: hidden;
    overflow-y: auto;
    padding: 2rem;
    gap: 2rem;
  }
</style>
