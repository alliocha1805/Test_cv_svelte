<script>
  import avatar from '$lib/images/avatar-shadow.png';

</script>

<div class="section">
    <img src={avatar} class="img_responsive" id=avatar alt="avatar">
    <div class="form_container">
        <form action="" method="get" class="form-example">
            <ul class="flex_outer">
                <li>
                    <label for="nom">Votre Nom</label>
                    <input type="text" id="nom_contact" placeholder="John Doe">
                </li>
                <li>
                    <label for="mail">Votre Mail</label>
                    <input type="mail" id="mail">
                </li>
                <li>
                    <label for="mail">Votre Message</label>
                    <textarea rows="6" id="message"></textarea>
                </li>
                <li>
                    <button type="submit">Envoyer</button>
                </li>
            </ul>
          </form>
    </div>

</div>