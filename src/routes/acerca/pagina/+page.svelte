<script>
import CardImage from "./CardImage.svelte"
</script>

<div class="pt-20 pb-10">
    <div class="mt-4 mx-14">
        <div>
            <div>
                <p class="font-semibold text-xl">Tecnologias usadas en la pagina:</p>
            </div>
            <div class="my-1 grid grid-cols-3 gap-2">

                <CardImage name="HTML 5" url="https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg"></CardImage>
                <CardImage name="JavaScript" url="https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png"></CardImage>
                <CardImage name="CSS" url="https://upload.wikimedia.org/wikipedia/commons/6/62/CSS3_logo.svg"></CardImage>
                <CardImage name="NodeJS" url="https://upload.wikimedia.org/wikipedia/commons/d/d9/Node.js_logo.svg"></CardImage>
                <CardImage name="Svelte Kit" url="https://upload.wikimedia.org/wikipedia/commons/1/1b/Svelte_Logo.svg"></CardImage>
                <CardImage name="Tailwind" url="https://tailwindcss.com/_next/static/media/tailwindcss-mark.3c5441fc7a190fb1800d4a5c7f07ba4b1345a9c8.svg"></CardImage>
            </div>
        </div>
    </div>
</div>