<script>
  import Layout from "./../Layout.svelte";
  import { basics } from "./../../models/cv.json";
  import GithubIcon from "./../icons/GitHub.svelte";
  import LinkedinIcon from "./../icons/LInkedin.svelte";
  import EmailIcon from "../icons/Email.svelte";

  const { label, name, lastName, location, phone, img } = basics;
  const { city, countryCode, region } = location;
</script>

<Layout title="">
  <div class="flex flex-col-reverse md:flex-row md:justify-between justify-center mt-5 items-center ">
    <div class="flex text-center md:text-start justify-start flex-col gap-2">
      <h2 class="text-3xl font-sans text-slate-800">
        {name}
        {lastName}
      </h2>
      <p class="text-slate-700 font-semibold">{label}</p>
      <div class="flex gap-2 justify-center md:justify-start mt-1">
        <p class="text-sm text-slate-600 text-center">
          {city}, {region}, {countryCode} |
        </p>
        <p class="text-sm text-slate-600">{phone}</p>
      </div>
      <div class="flex justify-center md:justify-start  text-slate-600 gap-1">
        <a
          href="https://github.com/devbryan02?tab=repositories"
          target="_blank"
          class="p-2 border rounded hover:bg-gray-200"
        >
          <GithubIcon />
        </a>
        <a
          href="https://www.linkedin.com/in/devbryan02/"
          target="_blank"
          class="p-2 border rounded hover:bg-gray-200"
        >
          <LinkedinIcon />
        </a>
        <a
          href="mailto:brayan7br7@gmail.com"
          target="_blank"
          class="p-2 border rounded hover:bg-gray-200"
        >
          <EmailIcon />
        </a>
      </div>
    </div>
    <div>
      <img
        src={img}
        alt="Img Not found"
        title="{name}Dev fachero detectado"
        width="100px"
        class="rounded-lg shadow-lg"
      />
    </div>
  </div>
</Layout>
