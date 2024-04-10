<script>
	import GitHub from './../icons/GitHub.svelte';
	import Git from './../icons/Git.svelte';
	import Tailwind from './../icons/Tailwind.svelte';
	import Css from './../icons/Css.svelte';
	import Mysql from './../icons/Mysql.svelte';
	import Html from './../icons/Html.svelte';
	import Spring from './../icons/Spring.svelte';
    import Java from "../icons/Java.svelte";
    import {skills} from './../../models/cv.json'
    import Layout from "../Layout.svelte";
    
</script>

<Layout title="Habilidades">
    <div class="flex justify-between my-5 flex-wrap">
        {#each skills as skill}
            <span class="text-sm text-slate-600 px-2 py-1 bg-gray-200 rounded cursor-pointer">
                {skill.name}
            </span>
        {/each}
    </div>
</Layout>