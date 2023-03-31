<script>
    import data from '$lib/json/compe-outil.json';
    let outilsRaw = data.outils;
    let size = 5; 
    let listeBlocOutils = [];
    for (let i=0; i<outilsRaw.length; i+=size) {
        listeBlocOutils.push(outilsRaw.slice(i,i+size));
        listeBlocOutils = listeBlocOutils;
}
</script>

<!--{console.log(compeRaw)}
{console.log(listeBlocCompetences)}-->
<div class="item" id="bloc_competence">
    {#each listeBlocOutils as blocOutil}
    <div class="bloc_compe">
        {#each blocOutil as outil}
        <!--{console.log(competence)} -->
        <div class=skill>
            <p>{outil.nom}</p>
            <div class="starblock">
                {#if outil.etoiles == 5}
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
                {:else if outil.etoiles == 4}
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
                {:else if outil.etoiles == 3}
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
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 32 29" fill="none">
                <path d="M16 0L19.5922 11.0557H31.2169L21.8123 17.8885L25.4046 28.9443L16 22.1115L6.59544 28.9443L10.1877 17.8885L0.783095 11.0557H12.4078L16 0Z" fill="#C4C4C4"/>
                </svg>
                {:else if outil.etoiles == 2}
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