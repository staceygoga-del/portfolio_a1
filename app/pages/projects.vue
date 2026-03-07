<script setup> 
import {ref,onMounted} from "vue"

const catFact = ref("")

    const getFact = async () => {
        const response = await fetch("https://catfact.ninja/fact")
        const data = await response.json()

        catFact.value = data.fact
    }

    onMounted(() => {
        getFact()
    })


</script>

<template>

    <div class="background">

        <nav>
            <div class="navbar">
                <NuxtLink to = "/"> Home </NuxtLink>
                <NuxtLink to = "/projects"> Projects </NuxtLink>
                <NuxtLink to = "/contacts"> Contact </NuxtLink>
            </div>
        </nav>
    <main>
    <h1> Projects </h1>
    <section class = "project-card">
    <h2> Comic Project </h2>
    <p>
        Created entirely from scratch, including full character design:
        head shapes, eye shapes, clothing textures, and accessories.
         The story follows a girl gifted a magical "thorn bag" from her grandmother.
        After defeating a monster, her powers unexpectedly emerge from her body, ending in a cliffhanger.
    </P>
    <p> <strong> Tools used: </strong> Procreate and Illustrator</p>
    <button>
    <a href = "/final comic.pdf" target="_blank">View Project</a>
    </button>
</section>

<section class = "project-card">
    <h2> Sims Website </h2>
    
    <p>  A functional website based on my Sims gameplay, created to showcase my web development skills.
        It demonstrates working HTML/CSS structure and interactivity.
    </P>

    <p><strong> Tools used: </strong> HTML, CSS and JavaScript</p>
    <div>
        <button> 
            <a href = "/Goga_Game/index.html" target="_blank"> View Project</a>
        </button>
    </div>
</section>

<section class = "project-card">
    <h2> Vacation Oasis - Travel Website</h2>
        <p>  
            Vacation Oasis was a collaborative group project where we designed and developed a travel-focused website highlighting popular lodges and resorts across South Africa. The website provided useful information for travelers, including seasonal weather patterns, available activities, and key details about each destination. The goal was to create an informative and user-friendly platform that helps users explore potential holiday destinations.
        </p>
        <p> <strong> Tools used: </strong> HTML, CSS and JavaScript </p>
        <h3>My Contribution</h3>
        <P>I was responsible for researching and organising information for specific destinations. This included adding details such as weather conditions during different seasons, available activities, and other relevant travel information to ensure each destination page was informative and well-structured.</P>
    </section>


    <section class="cat-fact">
        <h2>Random Cat Fact</h2>
        <p>{{ catFact }}</p>
        <button @click="getFact()"> Get another fact</button>
    </section>


</main>
<br>

</div>

</template>

<style scoped>
.cat-fact{
    max-width:600px;
    margin:60px auto;
    padding:30px;

    background:rgba(0,0,0,0.45);
    border:1px solid rgba(255,150,200,0.2);

    border-radius:20px;
    backdrop-filter:blur(10px);
    text-align:center;
}

.cat-fact h2{
    color: #ff9bcf;
    margin-bottom:15px;

}

.cat-fact p {
    line-height:1.6;
    margin:15px 0;
}

h1 {
    text-align:center;
    color: #ff9bcf;
}



</style>