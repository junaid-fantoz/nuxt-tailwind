<template>
    <div class="footer fixed bottom-0 flex items-center opacity-100 rounded-t-xl w-full h-24 px-5">
        <button class="btn btn-blue text-white w-full">
            <slot>Button</slot>
        </button>
    </div>
</template>

<style lang="postcss" scoped>
.footer {
    background: #FFFFFF 0% 0% no-repeat padding-box;
    box-shadow: 0px -1px 3px #00000033;
}
.btn {
  @apply font-bold py-2 px-4 rounded-xl;
  &.btn-blue {
    background: transparent linear-gradient(95deg, #319795 0%, #3182CE 100%) 0% 0% no-repeat padding-box;
  }
}
</style>