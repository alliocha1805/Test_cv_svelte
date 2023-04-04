<script>
import { onMount } from 'svelte';
let hamburger
let navMenu

onMount(() => {
  hamburger.addEventListener("click", () => {
    hamburger.classList.toggle("active");
    navMenu.classList.toggle("active");
  })

  document.querySelectorAll(".nav-link").forEach(n => n.addEventListener("click", () => {
    hamburger.classList.remove("active");
    navMenu.classList.remove("active");
  }))
};
</script>

<header>
   <div class="containerNav"> 
      <nav class="navbar">
         <a href="#" class="nav-branding">DEV</a>
         <ul bind:this={navMenu} class="nav-menu">
            <li class="nav-item">
               <a href="#Informations">Informations</a>
            </li>
            <li class="nav-item">
               <a href="#experiences">Expériences</a>
            </li>
            <li class="nav-item">
               <a href="#Education">Education</a>
            </li>
            <li class="nav-item">
               <a href="#Competences">Compétences</a>
            </li>
            <li class="nav-item">
               <a href="#Projets">Projets</a>
            </li>
         </ul>
         <div bind:this={hamburger} class="hamburger">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
         </div>
      </nav>
   </div>
</header>




<style>
*{
  padding: 0;
  margin: 0;
}
header{
  background-color: #2f4858;
}
li{
  list-style: none;
}
a{
  color: white;
  text-decoration: none;
}
.containerNav{
  max-width: 1224px;
  width: 90%;
  margin: 0 auto;
}
.navbar{
  min-height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav-branding{
  font-size: 2rem;
}
.nav-menu{
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 60px;
}
.nav-link{
  transition: 0.3s ease-out;
}
.nav-link:hover{
  color: dodgerblue;
}
.hamburger{
  display: none;
  cursor: pointer;
}
.bar{
  display: block;
  width: 25px;
  height: 3px;
  margin: 5px auto;
  -webkit-transition: all 0.3s ease;
  transition: all 0.3s ease;
  background-color: white;
}

@media(max-width:800px){
  .hamburger{
    display: block;
  }
 .hamburger.active .bar:nth-child(2){
    opacity: 0;
  }
 .hamburger.active .bar:nth-child(1){
    transform: translateY(8px) rotate(45deg);
  }
 .hamburger.active .bar:nth-child(3){
    transform: translateY(-8px) rotate(-45deg);
  }
 .nav-menu{
    position: fixed;
    left: -100%;
    top: 70px;
    gap: 0;
    flex-direction: column;
    background-color: #262626;
    width: 100%;
    text-align: center;
    transition: 0.3s;
  }
 .nav-item{
    margin: 16px 0;
  }
 .nav-menu.active{
    left: 0;
  }
}
</style>