<script>

    import Layout from "./../Layout.svelte";
    import { basics } from "./../../models/cv.json";
    import GithubIcon from "./../icons/GitHub.svelte";
    import LinkedinIcon from "./../icons/LInkedin.svelte";
    import EmailIcon from "../icons/Email.svelte";

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
            <p class="text-slate-700 font-bold">{label}</p>
            <div class="flex gap-2 mt-1">
                <p class="text-sm text-slate-600">
                    {city}, {region}, {countryCode} |
                </p>
                <p class="text-sm text-slate-600">{phone} </p>
            </div>
            <div class="flex text-slate-600 gap-1">
                <a
                    href="https://github.com/bryanby2002?tab=repositories"
                    target="_blank"
                    class="p-2 border rounded hover:bg-slate-200"
                >
                    <GithubIcon />
                </a>
                <a
                    href="https://www.linkedin.com/in/bryanby2002/"
                    target="_blank"
                    class="p-2 border rounded hover:bg-slate-200"
                >
                    <LinkedinIcon />
                </a>
                <a
                    href="mailto:brayan7br7@gmail.com"
                    target="_blank"
                    class="p-2 border rounded hover:bg-slate-200"
                >
                    <EmailIcon/>
                </a>
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
