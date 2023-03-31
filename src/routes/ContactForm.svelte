<script>
  import avatar from '$lib/images/avatar-shadow.png';
  // on va utiliser le site https://www.staticforms.xyz/ pour ca
  let accessKey = "6d1aa301-64d7-4c67-90e0-7cc299f0c009"
  let formSubmitted = false;
  const submitForm = () => formSubmitted = true; 
</script>

<div class="section">
    <img src={avatar} class="img_responsive" id=avatar alt="avatar">
    <div class="form_container">
        {#if !formSubmitted}
        <form action="https://api.staticforms.xyz/submit" method="post" class="form-example" on:submit|preventDefault={submitForm}>
            <input type="hidden" name="accessKey" value={accessKey}>
            <ul class="flex_outer">
                <li>
                    <label for="nom">Votre Nom</label>
                    <input type="text" id="nom_contact" name="name" placeholder="John Doe">
                </li>
                <li>
                    <label for="mail">Votre Mail</label>
                    <input type="mail" id="mail" name="email">
                </li>
                <li>
                    <label for="mail">Sujet</label>
                    <input type="text" id="sujet" name="subject">
                </li>
                <li>
                    <label for="mail">Votre Message</label>
                    <textarea rows="6" id="message" name="message"></textarea>
                </li>
                <input type="text" name="honeypot" style="display: none;">
                <li>
                    <button type="submit">Envoyer</button>
                </li>
            </ul>
          </form>
          {:else}
            <p>Merci pour votre message</p>
          {/if}
    </div>

</div>