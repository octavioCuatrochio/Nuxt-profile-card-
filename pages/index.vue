<template>
  <div class="container emp-profile">
    <form method="post">
      <div class="row">
        <ProfileImage :source="img"></ProfileImage>

        <ProfileHeader :complete_name="name" :role="role" :ranking="ranking"></ProfileHeader>
        <div class="col-md-2">
          <Button>Edit Profile</Button>
        </div>
      </div>
      <div class="row">
        <ProfileInfo :family_info="family_items" :education_info="education_items"></ProfileInfo>

        <ProfileInfoTab :info="aditional_info"></ProfileInfoTab>
      </div>
    </form>
  </div>
</template>

<script>
import ProfileHeader from '../components/profile/ProfileHeader.vue';
import ProfileInfo from '../components/profile/ProfileInfo.vue';
import ProfileInfoTab from '../components/profile/ProfileInfoTab.vue';
import ProfileImage from '../components/profile/ProfileImage.vue';
import Button from '../components/UI/Button.vue';

export default {
  name: "IndexPage",
  components: { ProfileHeader, ProfileInfo, ProfileInfoTab, ProfileImage, Button },
  data() {
    return {
      name: 'Kshiti Ghelani',
      role: 'Web Developer and Designer',
      img: "https://thumbs.dreamstime.com/b/perfil-de-usuario-vectorial-avatar-predeterminado-179376714.jpg",
      ranking: '8',
      family_items: [
        { name: "Children" },
        { name: "married" }
      ],
      education_items: [
        { name: "University" },
        { name: "Middle School" },
        { name: "College" }
      ],
      aditional_info: {
        phone: "1234",
        username: "placeholder",
        name: "placeholder",
        email: "palceholder@gmail.com"
      }
    }
  },
  async fetch() {
    this.mountains = await fetch(
      'https://randomuser.me/api/'
    ).then(res => res.json()).then(data => {

      // easier access
      let shortData = data.results[0];

      // adquire title, first and last name of the person
      let names = shortData.name;
      this.name = names.title + " " + names.first + " " + names.last;

      this.img = shortData.picture.large;

      // aditional info for tabs
      this.aditional_info = {
        phone: shortData.cell,
        username: shortData.login.username,
        name: this.name,
        email: shortData.email
      }
    });
  }
}
</script>

<style>
body {
  background: -webkit-linear-gradient(left, #3931af, #00c6ff);
  overflow-y: hidden;
}

.emp-profile {
  padding: 3%;
  margin-top: 3%;
  margin-bottom: 3%;
  border-radius: 0.5rem;
  background: #fff;
}
</style>