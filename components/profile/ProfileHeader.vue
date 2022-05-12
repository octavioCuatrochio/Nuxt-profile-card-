<template>
    <div class="col-md-6">


        <div class="profile-head">
            <h5>
                {{ complete_name }}
            </h5>
            <h6>
                {{ role }}
            </h6>
            <p class="profile-rating">RANKINGS : <span>{{ ranking }}/10</span></p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProfileHeader',
    props: ['complete_name', 'role', 'ranking']
}
</script>

<style>
.profile-rating {
    font-size: 12px;
    color: #818182;
    margin-top: 5%;
}

.profile-rating span {
    color: #495057;
    font-size: 15px;
    font-weight: 600;
}


.profile-head h5 {
    color: #333;
}

.profile-head h6 {
    color: #0062cc;
}

.profile-head .nav-tabs {
    margin-bottom: 5%;
}

.profile-head .nav-tabs .nav-link {
    font-weight: 600;
    border: none;
}

.profile-head .nav-tabs .nav-link.active {
    border: none;
    border-bottom: 2px solid #0062cc;
}
</style>