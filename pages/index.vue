<template>
  <div>
    <NuxtLink to="home">
      <div class="round-shaped-header absolute -left-12 -top-12"></div>
    </NuxtLink>
    <div class="absolute bottom-0 right-0 tracking-wider heading-bottom-right">
      Test Mobile Index ALL
    </div>
  </div>
</template>

<style scoped lang="postcss">
.heading-bottom-right {
  width: 240px;
  opacity: 1;
  font-size: 75px;
  color: #319795;
}

.round-shaped-header {
  width: 168px;
  height: 168px;
  background: #f00 0% 0% no-repeat padding-box;
  border: 1px solid #707070;
  opacity: 1;
  border-radius: 50%;
}
</style>