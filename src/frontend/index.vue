<template>
    <p>Hello World!</p>
</template>

<script setup>
    const { data, pending, error, refresh } = await useAsyncData('Key', () => $fetch('URL', {
        method: 'HTTPメソッド',
        headers: {'': ''},
        params: {'': ''}
    }))

    console.log(data.value)
</script>
