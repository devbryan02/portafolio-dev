<script>
  import { skills } from "./../../models/cv.json";
  import Layout from "../Layout.svelte";
</script>

<Layout title="Habilidades">
  <div class="flex flex-col md:flex-row gap-1 justify-between my-5 flex-wrap">
    {#each skills as skill}
      <a
        href="#tecnologias"
        title={skill.keyword+ " | "+skill.level}
        class="text-sm text-slate-600 px-2 py-1 border-2 border-dashed rounded-lg 
        cursor-pointer text-center md:text-start hover:border-solid"
      >
        {skill.name}
      </a>
    {/each}
  </div>
</Layout>
