
<script setup> 
/*Stacey Goga u25120702*/
import {ref,onMounted} from 'vue'

const temperature  = ref("")
const windspeed = ref("")

    const getTemperature = async () => {
        const response = await fetch("https://api.open-meteo.com/v1/forecast?latitude=-25.7479&longitude=28.2293&current_weather=true")
        const data = await response.json()
        temperature.value = data.current_weather.temperature
        windspeed.value = data.current_weather.windspeed

    }

    onMounted(() => {
        getTemperature()
    })


</script>

<template>
    <div class="background">
    <nav>
        <div class ="navbar">
            <NuxtLink to = "/"> Home </NuxtLink>
            <NuxtLink to = "/projects"> Projects </NuxtLink>
             <NuxtLink to = "/contacts"> Contact </NuxtLink>
        </div>
    </nav>
    <br>

    <div class="weather-card">
            <p>Current Weather in Pretoria</p>
            <p>Temperature: {{ temperature }}°C</p>
            <p>Wind Speed: {{ windspeed }} km/h </p>
    </div>

    <main>
        <section class="intro-card">
    <section class = "hero">
        <div class=" hero-container">

            <div class = "hero-text">
                <h1>Stacey Goga</h1>
       
                <h2> Multimedia Student | Web & Game Development Enthusiast</h2>
                <p> Building Interactive and visually engaging digital experience. </p>

                <NuxtLink to="/projects">
            <button> View Projects </button>
                </NuxtLink>
            </div>

            <div>
                <img src="/photo.jpg" alt="photo of Stacey" class="portfolio-photo">
            </div>

        </div>
    </section>

    <section class = "me">
        <div class = "heading">
        <h2>Meet Stacey</h2>
        </div>
    <div>
<p>
    I’m a second-year Multimedia student at the University of Pretoria pursuing a Bachelor of Information Science. 
    I’m passionate about web development, software development, and UX/UI design, and I enjoy building digital experiences that combine creativity with technology. 
    I’m currently developing my programming skills while exploring areas such as game development and interactive media. 
    Outside of tech, I enjoy painting, reading, and gaming, which often inspire my creative work.
</p>

         </div>


         <br>

    </section>
</section>

    <section class = "skills">
        <div class = "heading">
            <h2>Skills</h2>
        </div>
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
            <li>UI/UX Design</li>
            <li>Adobe Creative Suite</li>
            <li>Beginner Programming(C++)</li>
        </ul>

    </section>
</main>

</div>
</template>

<style > 
  
</style>