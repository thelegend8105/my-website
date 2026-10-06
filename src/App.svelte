<script>
  import ProfileSection from "./lib/ProfileSection.svelte";
  import DataSection from "./lib/DataSection.svelte";

  const data = [
    {
      title: "Experience",
      data: [
        {
          title: "Intern at Herschel Infrared Ltd. UK",
          description:
            "Worked on integrating weather data into the system and did frontend work for the desktop application.",
          link: "https://www.herschel-infrared.co.uk/",
          year: 2026,
        },
      ],
    },
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
        {
          title: "Skycast AI",
          description: "An app to predict weather",
          link: "https://github.com/thelegend8105/ai-project",
          year: 2026,
        },
        {
          title: "Self-healing AI-ops",
          description: "An experimental self-healing application using AI",
          link: "https://github.com/thelegend8105/healing-aiops",
          year: 2026,
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
    max-width: 768px;
    width: 100%;
    overflow-x: hidden;
    padding: 2rem;
    gap: 2rem;
  }
</style>
