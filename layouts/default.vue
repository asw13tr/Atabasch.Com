<template>
    <Navbar  />
<div class="container">
    <slot />
</div>
</template>

<script setup>
useHead({
    link: [
        { rel:'stylesheet', href: '/styles/default.css' }
    ],
    htmlAttrs: {
        lang: 'tr',
        'data-bs-theme': 'dark'
    },
    bodyAttrs: {
        class: '',
        style: 'background-color: #0F172A;'
    }
})
</script>
