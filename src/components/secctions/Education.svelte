<script>
    import {education} from './../../models/cv.json'
    import Layout from '../Layout.svelte';

    const {instition, area, endDate, startDate, url}  = education
</script>

<Layout title="Education">
    <div class="flex justify-between mt-5">
        <p class="text-sm text-slate-700 font-bold">{instition}</p>
        <p class="text-sm text-slate-500">{startDate} - {endDate}</p>
    </div>
    <p class="text-sm text-slate-600">{area}</p>
</Layout>

