<script>
    import Layout from "../Layout.svelte";
    import {skills} from './../../models/cv.json'
</script>

<Layout title="Habilidades">
    <div class="flex gap-2 my-5 flex-wrap">
        {#each skills as skill}
            <span class="text-sm text-slate-600 px-2 py-1 bg-gray-200 rounded cursor-pointer">
                {skill.name}
            </span>
        {/each}
    </div>
</Layout>