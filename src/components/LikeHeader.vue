<template>
    <div>
        <slot name="title"></slot>
        <hr>
        <slot></slot>
        <hr>
        <p>いいねの数</p>
        <slot name="number"></slot>
        <hr>
    </div>
</template>

<script>
export default {
    props: ['headerText']
}
</script>