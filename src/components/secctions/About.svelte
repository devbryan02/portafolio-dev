<script>

    import Layout from "../Layout.svelte";
    import {basics} from './../../models/cv.json'

    const {sumary} = basics
</script>


<Layout title= "Sobre mi">
    <p class="text-sm text-slate-700 text-justify mt-2">{sumary}</p>
</Layout>