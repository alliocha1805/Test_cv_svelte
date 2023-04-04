<script>

</script>

<nav id="navbar">
    <ul>
        <li><a href="#Informations">Informations</a></li>
        <li><a href="#experiences">Expériences</a></li>
        <li><a href="#Education">Education</a></li>
        <li><a href="#Competences">Compétences</a></li>
        <li><a href="#Projets">Projets</a></li>
    </ul>
</nav>

<style>
nav {
	width: 100%;
	margin: 0 auto;
	background-color: #2f4858;
	position: sticky;
	top: 0px;
	z-index: 999999;
}
nav ul {
	list-style-type: none;
	margin-block-start: 0;
	margin-block-end: 0;
	height: inherit;
}
nav ul li {
	float: left;
	width: 20%;
	text-align: center;
	position: relative;
	height: inherit;
}
nav ul::after {
	content: '';
	display: table;
	clear: both;
}
nav a {
	display: block;
	text-decoration: none;
	color: white;
	border-bottom: 2px solid transparent;
	padding: 10px 0px;
	font-family: 'Roboto', sans-serif;
	height: 50%;
}
nav a:hover {
	color: white;
	border-bottom: 5px solid white;
}

@media only screen and (max-width: 768px) {
	nav ul {
		flex-direction: column;
	}
	nav ul li {
		text-align: center;
	}
	#navbar ul {
		display: none;
	}
}
</style>