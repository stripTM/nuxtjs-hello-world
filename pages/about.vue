<template>
  <div>
    <h1>Acerca de</h1>
    <p>Hola desde {{ name }}</p>
    <NLink to="/">
      Portadas
    </NLink>
  </div>
</template>

<script>
export default {
  asyncData () {
    return {
      name: process.static ? 'Estático' : (process.server ? 'server' : 'Cliente')
    }
  },
  head: {
    title: 'Página de acerca de'
  }
}
</script>
