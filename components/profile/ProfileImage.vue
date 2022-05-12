<template>
    <div class="col-md-4">
        <div class="profile-img">
            <img :src="source" alt="" />
            <div class="file btn btn-lg btn-primary">
                Change Photo
                <input type="file" name="file" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ProfileImage",
    props: ['source'],
}
</script>

<style>
.profile-img {
    text-align: center;
}

.profile-img img {
    width: 70%;
    height: 100%;
}

.profile-img .file {
    position: relative;
    overflow: hidden;
    margin-top: -20%;
    width: 70%;
    border: none;
    border-radius: 0;
    font-size: 15px;
    background: #212529b8;
}

.profile-img .file input {
    position: absolute;
    opacity: 0;
    right: 0;
    top: 0;
}
</style>