<template>
    <button
        v-if="value != null"
        v-clipboard="value"
        class="slds-button slds-button_icon slds-cell-edit__button slds-m-left_x-small"
        title="Copy to clipboard">

        <svg
            class="slds-button__icon slds-button__icon_hint slds-button__icon_edit"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 24 24"
            width="100%"
            height="100%">
            <path d="M8 5.4h8c.4 0 .8-.4.8-.8V3.1c0-1.2-1-2.2-2.2-2.2H9.5c-1.2 0-2.2 1-2.2 2.2v1.5c0 .4.3.8.7.8zm12-2.6h-.8c-.2 0-.3.1-.3.3v1.5c0 1.6-1.3 3-2.9 3H8c-1.6 0-2.9-1.4-2.9-3V3.1c0-.2-.1-.3-.3-.3H4c-1.2 0-2.2 1-2.2 2.2v15.9c0 1.2 1 2.2 2.2 2.2h16c1.2 0 2.2-1 2.2-2.2V5c0-1.2-1-2.2-2.2-2.2z"/>
        </svg>

    </button>
</template>

<script>
    export default {
        props: {
            value: {}
        },
    }
</script>

<style scoped lang="scss">

    .slds-button_icon {

        &:active {
            animation: click-effect 120ms cubic-bezier(1, 1.9, 0.94, 0.98);
        }
    }

    @keyframes click-effect {

        25% {
            transform: scale(0.94, 0.94);
        }

        100% {
            transform: scale(0.98, 0.98);
        }
    }

</style>
