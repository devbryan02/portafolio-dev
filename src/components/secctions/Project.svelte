<script>
  import Layout from "../Layout.svelte";
  import { projects } from "./../../models/cv.json";
</script>

<Layout title="Proyectos">
  <div class="flex flex-row flex-wrap gap-2 justify-start w-full mt-5">
    {#each projects as project}
      <article class="p-5 border-2 border-dashed rounded-lg w-auto">
        <div class="flex gap-1 justify-between items-center">
          <p class="text-sm font-bold dark:text-[#DFDFD6] text-slate-700 py-2 hover:underline">
            <a href={project.url} target="_blank" title="Ver en GiHub"
              >{project.name}</a
            >
          </p>
          <p class="text-sm dark:text-[#DFDFD6] text-slate-500">
            {project.startDate} - {project.endDate}
          </p>
        </div>
        <p class="text-sm dark:text-[#DFDFD6] text-slate-600 text-justify">{project.description}</p>
        <div class="flex flex-col gap-2">
          <p class=" dark:text-[#DFDFD6] text-slate-800 font-bold text-sm mt-2">Tecnologias:</p>
          <div class="flex flex-col md:flex-row gap-2 flex-wrap">
            {#each project.tecnologys as tecnology}
              <a
                class="text-sm hover:text-gray-900 px-3 p-1 border border-dashed rounded-lg hover:bg-gray-200 text-center md:text-start"
                href={tecnology.url}
                target="_blank"
                title="visitar {tecnology.url}"> {tecnology.name}</a
              >
            {/each}
          </div>
        </div>
      </article>
    {/each}
  </div>
</Layout>
