<script>
	import avatar from '$lib/images/avatar-shadow.png';
    import NavBar from './NavBar.svelte';
    import NavBar2 from './Navbar2.svelte';
    import ContactForm from './ContactForm.svelte';
    import Experiences from './Experiences.svelte';
    import Formation from './Formation.svelte';
    import Competences from './Competences.svelte';
    import Outils from './Outils.svelte';
    import Projets from './Projets.svelte';
</script>

<svelte:head>
	<title>Alexis PILOY - Product Owner</title>
	<link rel="preconnect" href="fonts.gstatic.com">
	<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap" rel="stylesheet">
</svelte:head>

<body style="margin: 0;">
        <!--Intro en mode Hero Banner-->
        <!--<div class="container" id="hero">
            <div class="item" id="entete">
                <p id="nom">Alexis Piloy</p>
                <p id="fonction">Product Owner</p>
            </div>
            <div class="item" id="go_down_head">
                <a href=#Informations style="width: 32px; align-self: center;">
                    <svg width="32px" height="32px" viewBox="0 0 58 44" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M2 1.86108L28.0559 41.3046L56 1.86108" stroke="white" stroke-width="5"/>
                    </svg>
                </a>
            </div>
        </div>-->
        <!--Menu-->
        <NavBar2 />
        <!--Bouton retour au top-->
        <button onclick="topFunction()" id="goBackTop" title="Go to top"><svg width="24px" height="24px" viewBox="0 0 58 44" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M56 42.4435L29.9441 2.99996L2 42.4435" stroke="white" stroke-width="3"/></svg></button>
        <!--Bloc Informations-->
        <div class="container" id="Informations">
            <div class="item" id="avatar">
                <img src={avatar} class="img_responsive" alt="avatar">
            </div>
            <div class="item" id="Informations_texte">
                <p><span style="font-family: 'Roboto', sans-serif; font-size: 32px;font-weight: bold;">Alexis Piloy</span><br>
                <span style="font-family: 'Roboto', sans-serif; font-size: 24px;font-weight: bold;">Product Owner</span></p>
                <p style="font-family: 'Roboto', sans-serif; font-size: 18px; text-align: justify;">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin vitae nulla bibendum magna rhoncus convallis vel eget eros. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam accumsan metus sit amet magna semper, et ultricies eros accumsan. Nullam condimentum ut libero nec consequat. Aliquam erat volutpat. Morbi vulputate eros sit amet eleifend finibus. Cras congue nisl eget mauris luctus, a tristique neque maximus. Suspendisse porttitor auctor gravida. Nam vel augue pretium nunc efficitur vulputate. Nulla vitae risus non dolor finibus blandit vitae vel orci.</p>
                <p><a href="https://www.linkedin.com/in/alexis-piloy/" target="_blank" style ="color: grey; text-decoration: underline;" rel="external nofollow">Linkedin</a> / <a href="https://github.com/alliocha1805" target="_blank" style ="color: grey; text-decoration: underline;" rel="external nofollow">Github</a></p>
                <a href=# class="bouton" id="download_cv_button" style="margin-bottom: 10px;">Télécharger mon CV</a>
                <a href="#Contact" class="bouton" style="margin-bottom: 10px;">Me contacter</a>
            </div>
        </div>
        <!--Bloc Expériences-->
        <div class="container" id="experiences">
            <div class="item">
                <h2>Expériences</h2>
                <Experiences />
            </div>
        </div>
        <!--Bloc Education-->
        <div class="container" id="Education">
            <div class="item">
                <h2>Education</h2>
                <Formation />
            </div>
        </div>
        <!--Bloc Competences-->
        <div class="container" id="Competences">
            <div class="item">
                <h2>Competences & Outils</h2>
            </div>
            <h3>Compétences</h3>
            <Competences />
            <h3>Outils</h3>
            <Outils />
        </div>
        <!--Bloc Projets-->
        <div class="container" id="Projets">
            <div class="item">
                <h2>Projets</h2>
                <Projets />
            </div>
        </div>
        <!--Bloc Contact-->
        <div class="container" id="Contact">
            <div class="item">
                <h2>Contact</h2>
            </div>
        <ContactForm />
        </div>
        <script>
            //Get the button
            var mybutton = document.getElementById("goBackTop");
            
            window.onscroll = function() {scrollFunction()};
            
            function scrollFunction() {
              if((window.innerHeight + window.pageYOffset) >= document.body.offsetHeight - 10) {
                mybutton.style.display = "none";
              }
              else if (document.body.scrollTop > 1000 || document.documentElement.scrollTop > 1000) {
                mybutton.style.display = "block";
              } 
              else {
                mybutton.style.display = "none";
              }
            }
            
            // When the user clicks on the button, scroll to the top of the document
            function topFunction() {
                document.getElementById("Informations").scrollIntoView();
            }
            </script>
    </body>

<style>
</style>
