<script setup> 

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

    <h1> Contact me</h1>
    <form name="contact" method="POST" data-netlify="true" netlify> 
            <input type="hidden" name="form-name" value="contact">
        <div>
            <label for="name">  Name: </label>
            <br/>
            <input type = "text" name="name" id = "name" placeholder=" " required>
              <!-- <span class = "error" > Please enter your name</span>-->
        </div>

        <div> 
            <label for = "email"> Email:</label>
            <br/>
            <input type = "email" name="email" id = "email" placeholder=" " required>
          <!-- <span class = "error" > Please enter a valid email address</span>-->
        </div>

        <div>
            <label for = "message"> Message: </label>
            <textarea id="message" name="message" placeholder="Write yout message"> </textarea>
        </div>
    
        <button type ="submit">Submit</button>

    </form>
</div>

</template>

<style scoped> 

h1 {
    text-align:center;
    color: #ff9bcf;
    margin-bottom: 30px;
}

form {
    max-width:600px;
    margin:60px auto;
    padding:40px;
    
    background:rgba(0,0,0,0.45);
    border:1px solid rgba(255,150,200,0.2);

    border-radius:20px;
    backdrop-filter:blur(10px);
}

form div{
    margin-bottom:20px;

}
label {
    font-weight:500;
}

input[type="text"],
input[type="email"],
textarea {
    width:100%;
    padding:13px;
    border-radius:10px;
    border:1px solid rgba(255,255,255,0.1);
    background:#1a1a1aca;
    color:white;
    font-family:inherit;
    transition: all 0.3 ease;
}

input[type="text"]:hover,
input[type="email"]:hover,
textarea:hover {
    border:1px solid #ff9bcf;
    box-shadow:0 0 8px rgba(255,155,207,0.5);
}

textarea {
    min-height:120px;
    resize:vertical;
}



input[type="submit"]:hover {
    background:#f47fb9;
}

a {
    text-decoration:none;
    margin-right:20px;
    color:#ff9cbf;
}

.background{
    min-height:100vh;
    padding-top:60px;
}

input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
    outline:none;
    border:1px solid #ff9bcf;
    box-shadow:0 0 8px rgba(255,155,207,0.6);
}

</style>