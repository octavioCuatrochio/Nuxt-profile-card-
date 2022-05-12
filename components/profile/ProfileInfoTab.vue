<template>

    <div class="col-md-6">
        <b-tabs content-class="mt-3">
            <b-tab class="profile-tab" title="About" active>
                <div class="col-md-12 highlight">
                    <div class="row">
                        <div class="col-md-6">
                            <label>User Id</label>
                        </div>
                        <div class="col-md-6">
                            <p>{{ info.username }}</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>Name</label>
                        </div>
                        <div class="col-md-6">
                            <p>{{ info.name }}</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>Email</label>
                        </div>
                        <div class="col-md-6">
                            <p>{{ info.email }}</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>Phone</label>
                        </div>
                        <div class="col-md-6">
                            <p>{{ info.phone }}</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>Profession</label>
                        </div>
                        <div class="col-md-6">
                            <p>Web Developer and Designer</p>
                        </div>
                    </div>
                </div>
            </b-tab>

            <b-tab class="profile-tab" title="Timeline">
                <div class="col-md-12 highlight">
                    <div class="row">
                        <div class="col-md-6">
                            <label>Experience</label>
                        </div>
                        <div class="col-md-6">
                            <p>Expert</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>Hourly Rate</label>
                        </div>
                        <div class="col-md-6">
                            <p>10$/hr</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>Total Projects</label>
                        </div>
                        <div class="col-md-6">
                            <p>230</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>English Level</label>
                        </div>
                        <div class="col-md-6">
                            <p>Expert</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-6">
                            <label>Availability</label>
                        </div>
                        <div class="col-md-6">
                            <p>6 months</p>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-md-12">
                            <label>Your Bio</label><br />
                            <p>Your detail description</p>
                        </div>
                    </div>


                </div>

            </b-tab>
        </b-tabs>
    </div>
</template>

<script>
export default {
    name: "ProfileInfoTab",
    props: ['info']
}
</script>


<style>
.profile-tab {
    font-weight: 600;
    border: none;
}

.highlight>.row>div:last-child {
    color: #0062cc;
}

.nav-tabs {
    font-weight: 600;
    color: #0062cc;
}

.nav-item .nav-link.active {
    border: none;
    border-bottom: 2px solid #0062cc;
}
</style>