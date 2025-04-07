<template>
    <button class="btn">
        <slot> </slot>
    </button>
</template>

<!-- Scoped to this component -->
<style scoped> 
.btn {
    background: navy;
    color: seashell;
    border: none;
    cursor: pointer;
}
</style>