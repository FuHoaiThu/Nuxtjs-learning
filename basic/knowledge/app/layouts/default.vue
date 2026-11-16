<template>
  <div>
    <header>
      <h1>Header</h1>
      <nav>
        <ul>
          <li><nuxt-link to="/">Home</nuxt-link></li>
          <li><nuxt-link to="/contact">Contact</nuxt-link></li>

        </ul>
      </nav>
    </header>
    <hr />
    <slot />
  </div>
</template>
