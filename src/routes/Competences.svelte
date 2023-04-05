<script>
    import data from '$lib/json/compe-outil.json';
    let compeRaw = data.competences;
    let size = 5; 
    let listeBlocCompetences = [];
    for (let i=0; i<compeRaw.length; i+=size) {
        listeBlocCompetences.push(compeRaw.slice(i,i+size));
        listeBlocCompetences = listeBlocCompetences;
}
</script>

<div class="item" id="bloc_competence">
    {#each listeBlocCompetences as blocCompe}
    <div class="bloc_compe">
        {#each blocCompe as competence}
        <div class=skill>
            <p>{competence.nom}</p>
            <div class="starblock">
                {#if competence.etoiles == 5}
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                {:else if competence.etoiles == 4}
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                {:else if competence.etoiles == 3}
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                {:else if competence.etoiles == 2}
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                {:else}
                <svg width="24" height="24" viewBox="0 0 32 29" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#2F4858"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                {/if}
            </div>
        </div>
        {/each}
    </div>
    {/each}
</div>