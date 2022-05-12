<template>
    <div class="col-md-4">
        <div class="profile-work">
            <ProfileInfoSection :title="familyTitle" :items="family_info"></ProfileInfoSection>
            <ProfileInfoSection :title="educationTitle" :items="education_info"></ProfileInfoSection>
        </div>
    </div>
</template>

<script>
import ProfileInfoSection from './ProfileInfoSection.vue';
export default {
    name: "ProfileInfo",
    components: { ProfileInfoSection },
    props: ['family_info', 'education_info'],
    data() {
        return {
            familyTitle: 'FAMILY',
            educationTitle: 'EDUCATION'
        }
    }
}
</script>

<style>
.profile-work {
    padding: 14%;
    margin-top: -15%;
}
</style>