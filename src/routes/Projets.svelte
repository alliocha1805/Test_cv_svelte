<script>
  import projetVLC from '$lib/images/github.png';
</script>
<!-- Il fait une lightbox de projet , par exemple avec https://biggerpicture.henrygd.me/?ref=madewithsvelte.com -->
<div class="projectGrid">
  <div class="project">
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
      <button class="itemProject"><img src = {projetVLC} /></button>
  </div>
</div>

<style>
.projectGrid{
  display: flex;
	flex-direction: row;
	justify-content: center;
  flex-wrap : wrap;
  margin-bottom:25px;
}
.itemProject{
  margin:15px;
  padding:0px;
  border: none;
  cursor: pointer;
  appearance: none;
  background-color: inherit;
}
</style>