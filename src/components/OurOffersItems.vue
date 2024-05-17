<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>
      <p><slot name="paragraph"></slot></p>
    </div>
  </div>
</template>

<style scoped>
.item {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 20rem;
  min-width: 15rem;
  gap: 1.5rem;
}

.details {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  width: 100%;
  align-items: center;
}

i {
  display: block;
  width: 4rem;
  height: 4rem;
}

h3 {
  font-size: 1.2rem;
  font-family: Garnett;
  color: var(--clr-heading-primary);
  text-align: center;
}

p {
  font-size: 1rem;
  text-align: center;
}
</style>
