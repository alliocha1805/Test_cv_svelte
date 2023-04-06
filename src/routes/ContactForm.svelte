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
                <li class="champFormContact">
                    <label for="nom">Votre Nom</label>
                    <input type="text" id="nom_contact" name="name" placeholder="John Doe" required>
                </li>
                <li class="champFormContact">
                    <label for="mail">Votre Mail</label>
                    <input type="mail" id="mail" name="email" placeholder="John.Doe@piloy.fr" required>
                </li>
                <li class="champFormContact">
                    <label for="mail">Sujet</label>
                    <input type="text" id="sujet" name="subject" placeholder="Demande de contact" required>
                </li>
                <li class="champFormContact">
                    <label for="mail">Message</label>
                    <textarea rows="6" id="message" name="message" required></textarea>
                </li>
                <input type="text" name="honeypot" style="display: none;">
                <li class="champFormContact" id="ZoneboutonContact">
                    <button type="submit" id="boutonContact">Envoyer</button>
                </li>
            </ul>
          </form>
          {:else}
            <p>Merci pour votre message</p>
          {/if}
    </div>

</div>

<style>
.form_container{
    flex-grow:1;
}

.champFormContact
{
    margin: 10px;
    display : flex;
    flex-direction : row;
    justify-content: space-between;
}
input {
    width: 80%;
}
textarea{
    width: 80%;
}
#ZoneboutonContact{
    justify-content: flex-end;
}
#boutonContact{
    width:81%;
    height:3em;
    background-color : #2f4858;
    color: white;
}
@media (max-width: 800px) {
ul{
    padding:0;
}
label{
    width:20%;
}
}
</style>