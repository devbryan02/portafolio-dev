<script>
  import Layout from "../Layout.svelte";
  import { basics } from "./../../models/cv.json";

  const { sumary } = basics;
</script>

<Layout title="Sobre mi">
  <p class=" dark:text-[#DFDFD6] text-slate-600 text-start mt-2 text-sm">{sumary}</p>
</Layout>
