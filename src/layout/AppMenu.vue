<script setup>
import { ref } from 'vue';

import AppMenuItem from './AppMenuItem.vue';

const model = ref([
    {
        label: 'Licencias',
        items: [{ label: 'Licencias', icon: 'pi pi-fw pi-home', to: '/' }]
    },
    {
        label: 'Configuración',
        items: [{ label: 'Usuarios', icon: 'pi pi-fw pi-id-card', to: '/uikit/formlayout' }]
    }
]);
</script>

<template>
    <ul class="layout-menu">
        <template v-for="(item, i) in model" :key="item">
            <app-menu-item v-if="!item.separator" :item="item" :index="i"></app-menu-item>
            <li v-if="item.separator" class="menu-separator"></li>
        </template>
    </ul>
</template>

<style lang="scss" scoped></style>
