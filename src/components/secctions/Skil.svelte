<script>
    import {skills} from './../../models/cv.json'
    import Layout from "../Layout.svelte";
    
</script>

<Layout title="Habilidades">
    <div class="flex flex-col md:flex-row gap-1 justify-between my-5 flex-wrap">
        {#each skills as skill}
            <span class="text-sm text-slate-600 px-2 py-1 bg-gray-200 rounded cursor-pointer text-center md:text-start">
                {skill.name}
            </span>
        {/each}
    </div>
</Layout>