<script>
  import { education } from "./../../models/cv.json";
  import Layout from "../Layout.svelte";

  const { instition, area, endDate, startDate, url } = education;
</script>

<Layout title="Educación">
  <div class="flex justify-between mt-5">
    <a
      href={url}
      target="_blank"
      title="Vistar {url}"
      class="text-sm dark:text-[#DFDFD6] text-slate-700 font-bold hover:underline">
      {instition}
    </a>
    <p class="text-sm dark:text-[#DFDFD6] text-slate-500">{startDate} - {endDate}</p>
  </div>
  <p class="text-sm dark:text-[#DFDFD6] text-slate-600">{area}</p>
</Layout>
