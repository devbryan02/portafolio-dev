<script>
	import GitHub from './../icons/GitHub.svelte';

    import Layout from "./../Layout.svelte";
    import { basics } from "./../../models/cv.json";
    import GithubIcon from './../icons/GitHub.svelte'
    import LinkedinIcon from './../icons/LInkedin.svelte'


    const { label, name, lastName, location, phone, email, img } = basics;
    const { city, countryCode, region } = location;

</script>

<Layout title="">
    <div class="flex flex-col md:flex-row justify-around mt-5">
        <div class="flex flex-col gap-2">
            <h2 class="text-4xl font-sans font-bold text-slate-800">
                {name}
                {lastName}
            </h2>
            <p class="text-slate-700 font-bold ">{label}</p>
            <div class="flex gap-2 mt-1">
                <p class="text-sm text-slate-600">
                    {city}, {region}, {countryCode} |
                </p>
                <p class="text-sm text-slate-600">{phone} |</p>
                <a
                    class="text-sm text-slate-600"
                    target="_blank"
                    title="Envia un mensaje a {email}"
                    href="mailto:brayan7br7@gmail.com"
                >
                    {email}
                </a>
            </div>
            <div class="flex text-slate-600">
                <GithubIcon/>
                <LinkedinIcon/>
            </div>
        </div>
        <div>
            <img
                src={img}
                alt="Img Not found"
                title="{name}Dev fachero detectado"
                width="150px"
                class="rounded-lg shadow-lg"
            />
        </div>
    </div>
</Layout>
