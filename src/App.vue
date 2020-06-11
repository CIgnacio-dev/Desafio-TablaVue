<template>
  <div id="app">
     <h1 class="text-center">{{titulo}}</h1>

        <div class="container pt-5">
          <table class="table table-striped">
            <thead>
              <tr>
                <th scope="col">#</th>
                <th scope="col">Nombre</th>
                <th scope="col">Apellido</th>
                <th scope="col">Run</th>
                <th scope="col">Nacimiento</th>
                <th scope="col">Edad</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(user, index) in users" :key="index">
                <th scope="row">{{index}}</th>
                <td>{{user.nombre}}</td>
                <td>{{user.apellido}}</td>
                <td>{{user.run}}</td>
                <td>{{user.nacimiento}}</td>
                <td>{{user.edad}}</td>
              </tr>
            </tbody>
          </table>
        </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
        titulo: 'Tabla de usuarios',
        users: [
            {
                "nombre": "José",
                "apellido": "Pérez",
                "run": "123456-2",
                "nacimiento": "12-04-67",
                "edad": 52
            },
            {
                "nombre": "María",
                "apellido": "Rodríguez",
                "run": "654321-1",
                "nacimiento": "30-11-90",
                "edad": 29
            },
            {
                "nombre": "Manuel",
                "apellido": "Patiño",
                "run": "14223456-6",
                "nacimiento": "02-12-59",
                "edad": 60
            }
        ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
