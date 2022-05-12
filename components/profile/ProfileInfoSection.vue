<template>
    <div class="profile_info">
        <p class="profile_info-header">{{ title }}</p>
        <template v-for="item in items" >
            <a href="" :key="item.name">{{ item.name }}</a><br />
        </template>
    </div>
</template>

<script>
export default {
    name: 'ProfileInfoSection',
    props: ['title', 'items']
}
</script>

<style>
.profile_info-header {
    font-size: 12px;
    color: #818182;
    font-weight: 600;
    margin-top: 10%;
}

.profile_info a {
    text-decoration: none;
    color: #495057;
    font-weight: 600;
    font-size: 14px;
}
</style>