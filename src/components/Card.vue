<template>
    <div class="card">
        <slot name="img"></slot>
        <h6 class="card-desc my-auto">
            <slot name="desc"></slot>
        </h6>
    </div>
</template>
<style>
.card {
    width: 300px;
    height: 320px;
    color: #000;
    padding: 10px;
    border-radius: 10px;
}

.card img {
    border-radius: 5px;
    width: 100%;
    height: 200px;
}
</style>