<template>
    <button type="submit" class="profile-edit-btn">
        <slot />
    </button>
</template>

<script>
export default {
    name: "Button"
}
</script>

<style>
.profile-edit-btn {
    border: none;
    border-radius: 1.5rem;
    width: 70%;
    padding: 2%;
    font-weight: 600;
    color: #6c757d;
    cursor: pointer;
}
</style>