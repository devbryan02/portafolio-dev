<script>
  import Layout from "../Layout.svelte";
  import { basics } from "./../../models/cv.json";

  const { sumary } = basics;
</script>

<Layout title="Sobre mi">
  <p class=" text-slate-600 text-justify mt-2 text-sm">{sumary}</p>
</Layout>
