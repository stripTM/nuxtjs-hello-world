<template>
  <div>
    <h1>Acerca de</h1>
    <p>Hola desde <em>{{ name }}</em></p>
    <NLink to="/">
      Portadas
    </NLink>
  </div>
</template>

<script>
export default {
  asyncData () {
    return {
      name: process.static ? 'estático' : (process.server ? 'servidor' : 'cliente')
    }
  },
  head: {
    title: 'Página de acerca de'
  }
}
</script>
